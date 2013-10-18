## 综述

这个组件是[Bootstrap](http://getbootstrap.com/)的[ScrollSpy](http://getbootstrap.com/2.3.2/javascript.html#scrollspy)的Kissy移植版本

很多长页面都会设有区块锚点，用户通过页内导航条可以迅速导航到对应区块。相应地，当用户把scrollbar滚动到某个区块时相应的导航也应该会被置于激活状态。这是一个很常见的需求，这个组件实现了一个KISSY版的ScrollSpy。


* 版本：1.0
* 作者：七念
* 标签：navigator
* demo：[http://gallery.kissyui.com/scrollspy/1.0/demo/index.html](http://gallery.kissyui.com/scrollspy/1.0/demo/index.html)

## 初始化组件

    S.use('gallery/scrollspy/1.0/index', function (S, Scrollspy) {
         var scrollspy = new Scrollspy(ConfigOb);
    })

### config参数
    
    ConfigObj: {
        {Number} [ offset = 0 ] 距离scroll区域顶部的位移。
        {String} [ navContainer = "#s_index_r_nav" ] 导航区块的选择器。
        {String} [ activerSelector = ".nav li" ] 需要被激活的元素的选择器。
        {String} [ scrollArea = ".scrollspy-area" ] 内容区域的选择器。
        {String} [ navSelector = "#s_index_r_nav.nav li > a" ] 导航元素的选择器。
    }

### DOM结构

对DOM结构的要求是，在导航器中设置属性data-href,值为它所对应的内容区域的选择器. 例如：

    <ul class="nav nav-list" id="s_index_r_nav">
      <li><a data-href="#J_Home" href="#">Home</a></li>
      <li><a data-href="#J_Library" href="#">Library</a></li>
      <li><a data-href="#J_Application" href="#">Applications</a></li>
      <li><a data-href="#J_Profile" href="#">Profile</a></li>
      <li><a data-href="#J_Settings" href="#">Settings</a></li>
      <li><a data-href="#J_Help" href="#">Help</a></li>
    </ul>