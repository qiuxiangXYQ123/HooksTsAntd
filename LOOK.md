<!--
 * @file: 
 * @author:  xyq <qiuxiang_zhiyi@163.com>
-->
创建：npx create-react-app react-typescript-demo --typescript 
antd按需加载：
    yarn add @craco/craco
    <!-- package.json 的配置需要做如下修改 -->
    "scripts": {
    -   "start": "react-scripts start",
    +   "start": "craco start",
    -   "build": "react-scripts build",
    +   "build": "craco build",
    -   "test": "react-scripts test",
    +   "test": "craco test",
    }
    <!-- 然后在项目的根目录下创建一个 craco.config.js 用于修改默认配置: -->
    const CracoAntDesignPlugin = require('craco-antd');
    module.exports = {
    plugins: [
        {
        plugin: CracoAntDesignPlugin,
        options: {
            customizeTheme: {
            '@primary-color': '#1DA57A',
            },
        },
        },
    ],
    };
    <!-- 加载配置 -->
    npm add craco-antd
    npm add less-loader

加载 npm i --save-dev @types/react-router-dom
用  import { createBrowserHistory } from 'history'
    const browserHistory = createBrowserHistory()
    去除地址中的#

加载 npm install --save react-redux
加载持久性的redux    npm install redux-persist    //有点像是转换将redux转换成storage


解决跨域 npm install http-proxy-middleware --save-dev


加载axios  npm install axios --save
    // 添加请求拦截器
    axios.interceptors.request.use
    // 添加响应拦截器
    axios.interceptors.response.use