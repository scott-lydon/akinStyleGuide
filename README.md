# akinStyleGuide
An ongoing style guide for akin. 

1. less code is generally better
2. let naming conventions match designer/product naming conventions. 
3. If you create an interface (for other developers) make sure the interface strongly and succinctly conveys what the reusable part does. 
4. Make the interface predictable.  There shouldn't be surprise events that occur when a reusable part is called on. 
5. Opt for protocols instead of superclasses when possible. 
6. If a protocol isn't being used for callbacks, use functional programming with extensions instead.  
  ie: instead of `class ArrowButton: UIButton, Arrowable` or `extension UIButton { func arrowMethod() {}}`
