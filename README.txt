����������
	�˴�CFM module�ǹ�����openSUSE������
	�ں�version:2.6.22.5-31
	�ں�����·����/usr/src/linux-2.6.22.5-31
			���ڸ�·�������ں�Դ��
	gcc version:4.2.1
	GNU Make version:3.81
ʹ�ò��裺
	1.�����ں�Դ��
		����/usr/src/linux-2.6.22.5-31
			ִ�У�make menuconfig
			ִ�У�make
		ע������ȫ������
	2.����CFMԴ��(cfm-release-v1.1.tar.gz)
		��CFMԴ��copy��/usr/srcĿ¼��
		����/usr/src
			ִ�У�tar zxvf cfm-release-v1.1.tar.gz
		����/usr/src/cfm-release-v1.1
			ִ�У�make
	3.�����豸
			ִ�У�/bin/mknod /dev/cfmemulator   c 10  130
	4.����ģ�鵽�ں���
		����/usr/src/cfm-release-v1.1
			ִ�У�insmod cfmemulator.ko
	5.ͨ���û�̬�������
		����/usr/src/cfm-release-v1.1/app
			ͨ���޸�example.c�е����ݣ��������ں˴��ݲ��õ�ioctl cmd
			ִ�У�make
			ִ�У�./example
	6.ж��CFMģ��
		���ȹر��û�̬����
		Ȼ��
			ִ�У�rmmod cfmemulator
���䣺
	1.������ִ�������Ҫroot�û�Ȩ��
	2.�û�̬����˫������ģ������Port�������
	  ��example.c����TWONICѡ�1��ʾʹ��˫������0��ʾ1������������ʵ�������������
	3.FlowID��VlanID�Ķ�Ӧ��ϵΪ��FlowID=VlanID/10
	4.��recvfrom����Լ����͵İ�ץȡ���������Ҷ�������Դ��ַ�����Լ������ݰ��޷�����,
	  Ϊ�˼�����MD5���ƣ��Է��͵����ݰ�����MD5ֵ���洢��MD5ֵ������ѭ�����У���
	  �Խ��յ������ݰ�ͬ������MD5ֵ���뷢��ʱ�洢��MD5���н��бȽϣ���MD5ֵ�Ѵ��ڣ�֤�����Լ����������ݰ�������������
	5.��management API�Ĳ��Դ��룬��example.c�ж��У���TestCase�ĵ���ͬ��Ҳ�У�
	  �������ʱ��Ҫ������Ҫѡȡ��
�����˫�������ã�
	��ʼ����£�һ��Ϊ���������������в�������Ϊ˫������
	1.�ر����������Edit�˵��£�ѡ��Virtual Network Editor��ѡ��Host Virtual Network Mapping
	  ������VMnet��Windows������ӳ���ϵ����VMnet0����Ϊ��Bridged to �����network adapter����
	  ��VMnet9 ����Ϊ��Bridge to ��һ��network adapter��������¼�������ǵĶ�Ӧ��ϵ��Ӧ���˳���
	2.����Edit virtual machine setting�������������ϵ�Add ��ť��ѡ��Network Adapter��������һ����
	  Network connectionΪCustom��ѡ��VMnet9������Finished���˳������������һ����������ӡ�
	  ����Edit virtual machine setting����ѡ��ԭ����Network Adapter����������Network connectionΪ
	  Custom��ѡ��VMnet0������OK��
	3.���������SUSE������ϵͳ���������磬���һ���������ӣ�������IP��ַ��
	4.ifconfig���鿴���������eth��С����������Ӧ��WMnet0��eth�Ŵ����������Ӧ��WMnet9���ɵ�֪
	  eth��Windows�����Ķ�Ӧ�����

	ע��Ŀǰ��example.c��ʹ�õ���eth0��eth1��eth0��ӦPort1��eth1��ӦPort2��Ҫ����ʵ����������趨