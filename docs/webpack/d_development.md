# Development
webpack.config.mode: 'development'
개발을 위한 도구 설명, avoid using them in production

# Using source maps
webpack.config.devtool: "inline-source-map", 
error, warning 의 tracking 이 쉬워진다.
다른 옵션들도 있다.

# Choosing a Development Tool
package.scripts.watch: "webpack --watch",
watch 를 걸어두면 코드 변경사항을 감지하고 re-compile 한다.
webpack.config.plugins.[new CleanWebpackPlugin({ cleanStaleWebpackAssets: false })],
매번 다 지우지 않도록 하는 옵션같다.

# Using webpack-dev-server
npm install --save-dev webpack-dev-server
webpack.config.devServer: {contentBase: "./dist",},
package.start: "webpack-dev-server --open",
localhost:8080으로 dev server 를 돌린다!

# Using webpack-dev-middleware
npm install --save-dev express webpack-dev-middleware
webpack.config.output.publicPath: '/',
add server.js
package.scripts.server: "node server.js",