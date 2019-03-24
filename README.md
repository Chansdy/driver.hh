# driver.hh
#ifndef DRIVER_HH 
#define DRIVER_HH 
#include <string> 
#include <map> 
#include“parser.hh”
  //为Flex提供我们想要的yylex原型... 
#define YY_DECL \ 
  yy :: parser :: symbol_type yylex（driver＆drv）
// ...并为解析器声明它。
YY_DECL;
class driver
  {
  public:
  driver();
  std:map<std::string,int>变量；结果；
  int parse（const std::string &f);
  std::string file;//正在解析的文件名称
  bool trace_parsing;//是否生成解析器调试跟踪
  bool trace_scanning;//是否生成扫描程序调试跟踪器
  yy:location location;
  //处理扫描
  void scan_begin();
  void scan_end();
  
  
  
  
