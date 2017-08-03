# iOSTips
Tips of iOS develep

#页面悬浮效果
给view加一个背景视图，给背景视图的layer设置shadow

#页面悬浮效果code
let frame = self.bounds
let bgView = UIView(frame: CGRect(x: 5, y: 5, width: frame.size.width-10, height: frame.size.height-10))
bgView.backgroundColor = UIColor.white
bgView.layer.shadowOffset = CGSize(width: 1, height: 1)
bgView.layer.shadowColor = UIColor.black.cgColor
bgView.layer.shadowOpacity = 0.3
bgView.layer.cornerRadius = 5
self.addSubview(bgView)
self.sendSubview(toBack: bgView)

#在storyboard中A push B push C 之后，想要从C直接pop回A
从C牵一条线到A，设置跳转方法为present as popOver

#TabBarItem的图片移位问题
UIEdgeInsets(top: CGFloat, left: CGFloat, bottom: CGFloat, right: CGFloat)

tabBarItem.imageInsets = UIEdgeInsetsMake(5, 0, -5, 0);
注意，这里设置inset的时候，top和bottom，left和right一定要配对，否则会发生按钮点击后，图片不断被拉伸的情况。
另外还要注意一点就是：tabbar底部栏的高度默认是49，其中包括像素1的分隔线

#
