# akinStyleGuide
An ongoing style guide for akin. 

1. less code is generally better
2. let naming conventions match designer/product naming conventions. 
3. If you create an interface (for other developers) make sure the interface strongly and succinctly conveys what the reusable part does. 
4. Make the interface predictable.  There shouldn't be surprise events that occur when a reusable part is called on. 
5. Opt for protocols instead of superclasses when possible. 
6. If a protocol isn't being used for callbacks, use functional programming with extensions instead.  
  ie: instead of `class ArrowButton: UIButton, Arrowable` or `extension UIButton { func arrowMethod() {}}`


7. If method B is called by method A, place method B directly underneath method A if possible: 

```
    func updateContainer() {
        let rectOfCell = responseTV.rectForRow(at: IndexPath(row: 0, section: 0)),
        rectInView = responseTV.convert(rectOfCell, to: responseTV.superview)
        if rectInView.minY >= 0 {return}
        var alpha = abs(rectInView.minY) / rectInView.height
        if alpha > 1 { alpha = 1 }
        setTopContainerAlpha(alpha)
    }
    
    fileprivate func setTopContainerAlpha(_ alpha: CGFloat) {
```
