
## 前言
简介：账号密码登录通用组件，可自定义主题色，主题logo，直接引用

## 有疑问
微信搜索“慢慢向好”小程序，找客服反馈，相应问题。
				  

## 素材
[图片资源](https://pixabay.com)
 
## 开始使用
下载源码解压，复制`/components` 下的组件至项目根目录的 `/components` 文件夹下


`index.vue`的`script`加入如下部分：
```
import loginPassword from '@/components/ay-login/login-password.vue';
	export default {
		components: {
			loginPassword,

		},
		data() {
			return {
				themeColor : '#33CCCC',
				logoUrl:'https://cdn.pixabay.com/photo/2016/11/23/17/55/beach-1854072__340.jpg',
					
			}
		},
		onLoad() {
			let that = this;

		},

		methods: {
			loginFun(e){
				console.log('登录'+ JSON.stringify(e))
			},
		}
	}
```


`index.vue`的`template`加入如下部分：
```
<view >
		<loginPassword :themeColor="themeColor" :logoUrl="logoUrl"  @loginFun="loginFun"></loginPassword>
		
	</view>

```



引入阿里矢量图，复制示例源码`/style` 下的`/iconfont.css`至项目根目录的 `/style` 文件夹下(APP需在地址前加`https：`)，内容如下：

```
@font-face {font-family: "iconfont";
  src: url('//at.alicdn.com/t/font_2190080_5t8zjsl434i.eot?t=1609760820846'); /* IE9 */
  src: url('//at.alicdn.com/t/font_2190080_5t8zjsl434i.eot?t=1609760820846#iefix') format('embedded-opentype'), /* IE6-IE8 */
  url('data:application/x-font-woff2;charset=utf-8;base64,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') format('woff2'),
  url('//at.alicdn.com/t/font_2190080_5t8zjsl434i.woff?t=1609760820846') format('woff'),
  url('//at.alicdn.com/t/font_2190080_5t8zjsl434i.ttf?t=1609760820846') format('truetype'), /* chrome, firefox, opera, Safari, Android, iOS 4.2+ */
  url('//at.alicdn.com/t/font_2190080_5t8zjsl434i.svg?t=1609760820846#iconfont') format('svg'); /* iOS 4.1- */
}

.iconfont {
  font-family: "iconfont" !important;
  font-size: 16px;
  font-style: normal;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.icon-xuanzhong:before {
  content: "\e607";
}

.icon-icon-eye-open:before {
  content: "\e612";
}

.icon-icon-eye-close:before {
  content: "\e613";
}

.icon-weixuan:before {
  content: "\e65d";
}

.icon-gengduo2:before {
  content: "\e736";
}

.icon-sousuo:before {
  content: "\e66d";
}

.icon-shang3:before {
  content: "\e689";
}

.icon-xia:before {
  content: "\e65a";
}

.icon-you:before {
  content: "\e600";
}

.icon-tubiaozhizuo-:before {
  content: "\e605";
}

.icon-time:before {
  content: "\e619";
}

.icon-xiaoxi:before {
  content: "\e615";
}

.icon-daohangdizhi:before {
  content: "\e65e";
}

.icon-gouxuan:before {
  content: "\e6ce";
}

.icon-icon_fuben:before {
  content: "\e611";
}

```


页面`App.vue` 引入css
```
<style>
	/*每个页面公共css */
	@import './style/iconfont.css';
</style>
```

 