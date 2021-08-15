# fsdb2svg

## Features

Convert fsdb/vcd file to svg
将 fsdb/vcd 文件转换为 svg 图片

## Usage

```
python3 ./fsdb2svg.py -i data/demo.fsdb -r data/demo.rc
```

## Argument

`-c`,`--config` 指定配置文件
`-i`,`--input` 指定波形文件，支持 fsdb 或 vcd 格式
`-r`,`--rcfile` 指定 rc 文件

## Configuration

Section  | Item         | Description
-------  | ----         | -----------
vcd2json | `path_list`  | 指定需要转换的信号路径, 如果指定rcfile, 会被rcfile覆盖
vcd2json | `start_time` | 指定转换的开始时间, 如果指定rcfile, 会被rcfile覆盖
vcd2json | `end_time`   | 指定转换的结束时间, 如果指定rcfile, 会被rcfile覆盖
vcd2json | `wave_chunk` | 指定波形分块大小
wavedrom | `handle_overlap` | 指定文字发生重叠时处理方式, 支持hscale/abbrev两种方式
wavedrom | `hscale_value` | 指定默认的缩放比例, 默认1


## Requirments

- fsdb2vcd (波形文件为 fsdb 时需要 fsdb2vcd 转为vcd)

## TODO
[ ] 处理异步信号
[ ] 处理多时钟
[ ] 优化引用的代码质量

## Credits

https://github.com/nanamake/vcd2json
https://github.com/wallento/wavedrompy
