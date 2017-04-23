# autoRemoteSSH
This bash script help you auto connect to remote SSH server through  your springboard VPN server.


#####################################################################
# 
#  支持通过VPN登录内网服务器，并转发端口
#
#  step 1. 请配置参数: "need_you_config"
#  step 2. scp rsa文件到VPN跳板机
#  
#  ssh_yzt: params option
#  usage: ssh_yzt [--help] param_1 param_2
#  参数说明：
#  param_1 内网机器简写
#  param_2 本地转发端口

#  机器列表{
#  [156-www测试]
#  [201-www预发布]
#  [114-oa测试]
#  [126-体验]
#  [69-www发布机]
#  }
#####################################################################
# step 3. 
# vim ~/.bash_profile
# 
# step 4.
# ```copy code to this file
# #ssh XXX
# function ssh_XXX(){
#   /Users/freedom/Applications/XXX/vpn/myAutoSSH.sh $@
# }
# ```
# 
# step 5.
# source ~/.bash_profile
# 
# step 6. awesome!
# ssh_yzt --help
# 
#####################################################################