# elasticsearch��װ����
# ����1
�����ص�elasticsearch��ѹ��ָ��Ŀ¼
# ����2
����binĿ¼�µ�elasticsearch.bat�ļ�
# ����3
����http://localhost:9200/�鿴�Ƿ�װ�ɹ�
# ����4 ��װ���ӻ�����
����elasticsearch-head
# ����5 ��װgrunt�ͻ���, �谲װnode.js
npm install -g grunt -cli
# ����6 ��װelasticsearch-head����
��elasticsearch-head��װĿ¼ִ��npm install
# ����7 �鿴elasticsearch-head��װ�Ƿ�ɹ�
ִ��grunt server����elasticsearch-head, ����http://localhost:9100/�Ƿ�����
# ����8 �޸�elasticsearch�����ļ�
�޸�elasticsearch�����ļ�config/elasticsearch.yml,�ڵײ�׷��
http.cors.enabled: true
http.cors.allow-origin: "*"
node.master: true
node.data: true
����http.port: 9200, node.name: node-1��cluster.name: my-application��ע��, ��������elasticsearch
# ����9
��elasticsearch-head�Ŀ��ӻ���������elastisearch����, �鿴�Ƿ�����

