# RegionPicker
描述：实例化一个省市县三级联动选择选择器(包含行政区划代码数据)

使用方法：new RegionPicker(selector)
参数说明：
selector：选择器；

对像方法：
obj.getCurRegion();//取得当前地址对像信息，返回一个对像。

    返回对像说明：
    {
        "prov":"湖北省",//当前选择的行政区省份，空为未选择。
        "city":"武汉市",//当前选择的行政区市级，空为未选择。
        "county":"江汉区",//当前选择的行政区县级/或区级，空为未选择。
    }

    示例代码

    //html代码：
    <div id="container"></div>
    <button id="getadcode">测试获取当前选择</button>

    //javascript代码
    const address = new RegionPicker('#container');//实例化一个对像;

    //取得当前选择的地址信息
    document.querySelector('#getadcode').onclick = function () {
        let curRegion = address.getCurRegion();
        console.log(curRegion);
    };
