9-4  到审批服务中心报到   装环境   做了jzsp的两个相应布局的静态页 完成了首页  还差个列表页

9-5   完成了列表页   还差后台框架
base-css.html   很多table  form  buttons

springmvc+mybatis
新建dynamic web project
copy jar  配置文件

clean  run as

新建Class  命名空间com.wish.bonafides.controller  Index

各种注解
@Controller(对应Controller)  @RequestMapping(对应的映射)   @Autowired(service对象)
@Repository(ＤＡＯ)  @Service(Service类)  @RequestParam(请求参数获取)

页面传值给服务器
    get  @RequestParam()




9-6

    静态文件都放到static/css、scripts


9-7

        主从表生成解决方案
        菜单页，列表 详细信息页  从FrontController映射并返回结果centerGeneral和openContent


9-8


        com.wsframework.jeesaas.modules.cms.entity
        com.wsframework.jeesaas.modules.cms

        静态资源文件放在static\bonafides\css、js、img
        cms页面在WEB-INF\views\moduals\cms\front\themes\basic


        ArticleController

            @RequestMapping(value = "${adminPath}/cms/article")
            ${adminPath} 是在jeesaas.properties 设置的值，自动读取

            =========================文章编辑==============================
            localhost:8080/a/cms/article?category.id=25
            @RequestMapping(value = "form")
    public String form(Article article, Model model)

    @ModelAttribute("category")

    a/cms/category  栏目列表  @RequestMapping(value = {"list", ""})
    a/cms/form     栏目添加Form  office_id归属机构  Category("1")父栏目
    a/cms/save      栏目添加   ${adminPath}  redirect:" + adminPath + "/cms/category/";
    a/cms/treeData  获得栏目菜单json数据




