---
#
# Here you can change the text shown in the Home page before the Latest Posts section.
#
# Edit cayman-blog's home layout in _layouts instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
#
layout: home
---

Slurm(Simple Linux Utility for Resource Management， http://slurm.schedmd.com/ )是开源的、具有容错性和高度可扩展的Linux集群超级计算系统资源管理和作业调度系统。超级计算系统可利用Slurm对资源和作业进行管理，以避免相互干扰，提高运行效率。所有需运行的作业，无论是用于程序调试还是业务计算，都可以通过交互式并行 srun 、批处理式 sbatch 或分配式 salloc 等命令提交，提交后可以利用相关命令查询作业状态等。

Slurm采用slurmctld服务（守护进程）作为中心管理器用于监测资源和作业，为了提高可用性，还可以配置另一个备份冗余管理器。各计算节点需启动slurmd守护进程，以便被用于作为远程shell使用：等待作业、执行作业、返回状态、再等待更多作业。slurmdbd(Slurm DataBase Daemon)数据库守护进程（非必需，建议采用，也可以记录到纯文本中等），可以将多个slurm管理的集群的记账信息记录在同一个数据库中。还可以启用slurmrestd(Slurm REST API Daemon)服务（非必需），该服务可以通过REST API与Slurm进行交互，所有功能都对应的API。用户工具包含 srun 运行作业、 scancel 终止排队中或运行中的作业、 sinfo 查看系统状态、 squeue 查看作业状态、 sacct 查看运行中或结束了的作业及作业步信息等命令。 sview 命令可以图形化显示系统和作业状态（可含有网络拓扑）。 scontrol 作为管理工具，可以监控、修改集群的配置和状态信息等。用于管理数据库的命令是 sacctmgr ，可认证集群、有效用户、有效记账账户等

