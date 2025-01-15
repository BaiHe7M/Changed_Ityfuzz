# build


```bash
cargo build --release
```

# 使用


示例

```bash
cargo run --release -- evm -t '/home/junlin/test0114/*' --function-sequence-file '/path/to/.txt'
```

其他参照https://docs.ityfuzz.rs/

-t指定目标路径，至少应包含abi和bin  （命令行一定要带上星号）

--function-sequence-file指定初始函数序列即相应参数文件路径 .txt文件格式如下:指定函数名：参数1类型：参数1，参数2类型:参数2,

*EXAMPLE*

```txt
transfer:address:0x1234567890abcdef1234567890abcdef12345678,uint256:1000
transferFrom:address:0x1234567890abcdef1234567890abcdef12345678,address:0x1234567890abcdef1234567890abcdef12345678,uint256:500
approve:address:0x1234567890abcdef1234567890abcdef12345678,uint256:1000
approveAndCall:address:0x1234567890abcdef1234567890abcdef12345678,uint256:1000,string:"extra data"
freezeAccount:address:0x1234567890abcdef1234567890abcdef12345678,bool:true
transferOwnership:address:0x1234567890abcdef1234567890abcdef12345678
setPrices:uint256:100,uint256:200
setBuyOpen:bool:true
setSellOpen:bool:true
transferEth:uint256:10

```
