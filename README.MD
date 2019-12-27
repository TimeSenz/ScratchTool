## install

npm install -g yarn
npm install -g webpack
npm install -g webpack-dev-server

git clone git@github.com:TimeSenz/ScratchTool.git

cd scratch-gui
yarn install

运行webpack-dev-server --https，打开:https://127.0.0.1:8601/

cd ../scratch-vm
yarn install
yarn link
yarn add uglifyjs-webpack-plugin
yarn run watch

# 新开一个shell
cd scratch-gui
yarn link scratch-vm

完成yarn link scratch-vm之后，scratch-gui就会采用我们开发环境里的scratch-vm，而不是默认的scratch-vm. 这样一来我们就可以定制scratch-vm了
