## Layered architecture style

The layered architecture style are organized into logical horizontal layers, each layer performing a specific role within the application (such as
presentation logic or business logic). Although there are no specific restrictions in terms of the number and types of layers that must exist, most layered architectures
consist of four standard layers: presentation, business, persistence, and database.

Layers of Isolation
Each layer in the layered architecture style can be either closed or open.
- Closed layer: means that as a request moves top-down from layer to layer, the request cannot skip any layers, but rather must go through the layer immediately below it to get to the next layer
- Open Layer: Allow to bypass layers and go to the next one down

Layers of isolation concept means that changes made in one layer of the architecture generally don’t impact or affect components in other layers, providing the contracts between those layers remain unchanged.

### When user
Choice for small, simple applications or websites

### Advantages
- Each layer is remplazable just need to follow the contreacts (interfaces).
### Disavantages
- Is not possible encasulate all for example:add a fielt to a entity (data model) should be replicate to other layes.

