# Architectural Anti-Patterns

## Sinkhole anti-pattern
Describes the situation where requests flow through multiple layers of the architecture as simple pass-through processing with little or no logic performed within each layer. For example, assume the presentation layer responds to a request from the user to retrieve customer data. The presentation layer passes the request to the business layer, which simply passes the request to the persistence layer, which then makes a simple SQL call to the database layer to retrieve the customer data. The data is then passed all the way back up the stack with no additional processing or logic to aggregate, calculate, or transform the data. 

The 80-20 rule is usually a good practice to follow. For example, it is acceptable
if only 20 percent of the requests are sinkholes. However, if 80 percent of the requests
are sinkholes, it a good indicator that the layered architecture is not the correct architecture
style for the problem domain. Another approach to solving the architecture
sinkhole anti-pattern is to make all the layers in the architecture open.