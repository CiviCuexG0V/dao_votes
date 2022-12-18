# Simple DAO votes test

The file `GovernorContract.sol` is still on work, several reference can be found [here](https://docs.openzeppelin.com/contracts/4.x/wizard).

Feel free to edit or add new features or any ideas for this project.

# Require
- `Node`
- `truffle`
	```bash
	npm install truffle -g
	```
- `Ganache`

# Run
- 撰寫完合約之後，可以在 Cli 介面執行指令進行編譯

	```bash
	truffle compiler
	```

# Deploy
- 在 `migrations` 資料夾內建立部署檔案，每個檔案要對應到各自的合約，不同部署檔案之間的開頭都要用數字區分
- 舉例：對應到 `contracts/Box.sol`，建立一個 `1_deploy.js`
- 在 Cli 介面執行指令

	```bash
	truffle migrate
	```

- 部署完之後，可以打開 `Ganache` 程式，點選 `BLOCKS` 部分，檢查部署的合約



# Description

- `contracts`：用來存放智能合約的 `sol` 檔案
- `migrations`：用來撰寫部署智能合約的檔案
- `test`：用來放測試檔


# Enviroment settings

- 在 `truffle-config.js` 內，在 `networks` 內將 `development` 啟用

	```js
	// truffle-config.js
	networks: {
		development: {
			host: "127.0.0.1",     // Localhost (default: none)
			port: 8545,            // Standard Ethereum port (default: none)
			network_id: "*",       // Any network (default: none)
		},
	}
	```

- `port` 的部分，要記得對應到 `Ganache` 開啟後，顯示 `RPC Server` 的 `port`
- `network_id` 可以留著 `*`，也可以改成對應 `Ganache` 內的 `network id`
- 在 `truffle-config.js` 內，在 `compilers` 內設定 `solidity` 的版本，記得要跟合約內容採用的一樣
