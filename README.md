# smart_monkey_config
smart_monkey 的配置

此git是为[smart_monkey](https://github.com/vigossjjj/CrashMonkey4IOS)的配置项。经过部分处理，使之截屏可以压缩，点击数成最大。最大情况下去查找性能和闪退问题。


${bundleID}		替换成	bundleID
${UDID} 			替换成	设备UDID号 ($instruments -s devices 使用此命令查看设备UDID)
${cfg_path}		替换成  配置项的路径，也就是此git下custom_cfg路径
${output_path}	替换成	输出结果的路径


smart_monkey -a ${bundleID} -w {UDID} --compress-result 50% --detail-count 100 --drop-useless-img 100 -c ${cfg_path} -d ${output_path}


//示例:
smart_monkey -a com.husor.beibei -w a9c1e0e6db82205d0a2106c027a5af7227200a19 --compress-result 50% --detail-count 100 --drop-useless-img 100 -c /Users/lizy/Documents/工作/smart_monkey_config/custom_cfg -d /Users/lizy/Documents/工作/smart_monkey_config/beibei