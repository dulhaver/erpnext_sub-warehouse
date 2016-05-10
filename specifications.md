Specifications for development of a sub-warehouse feature for ERNext
----------------------------
The feature has to be merged upstream, therefore developers are expected to collaborate and consult with Frappé team in order to maintain necessary level of the code.

1. we should think in terms of **hierarchically stacked 'locations'** (no matter whether that's a warehouse, a shelf, a bin, etc. whose place inside such hierarchy is defined by it's 'parent' location. 
2. The **mother** or **root** warehouse of any stack just wouldn't have any 'parent' 
3. So having a 'parent' or not is a matter of choice rather then mandatory
4. there is a 'parent' field in each warehouse which by default is empty.
5. **location type** might be a value that has to be set (and the type should be something that can be defined) by the user. 
I guess warehouse might be the default value. Other types can be defined freely. Some default values should be 'warehouse', 'rack', ' shelf, 'bin'
6. **Virtual locations** should be possible. For example someone sends goods from A to be ... they can be in a virtual location (the truck) temporarily. Another usecase for a virtual location might be when raw materials are being used to manufacture something and during that time they are in the 'virtual' location of the production hall
7. being able to assign a **postal address** to a warehouse would be useful for anyone who deals with actually various location or even branches of a company. If such an address feature is going to be implemented it's default value should be "as parent". Only if that is not marked it'll be possible to add a specific address.
