# ���ø����û����ƺ͵����ʼ���ַ, --systtemΪ����ϵͳ����, --globalΪ���û�ȫ�ֱ���, ��Ϊ��ǰ��Ŀ����
git config --global user.name "�˻�"
git config --global user.email "����"

# �ڵ�ǰ�ļ����´����ֿ�
git init
# ָ���ļ��д����ֿ�
git init �ֿ���
# ��¡Զ�ֿ̲�
git clone repository��ַ
# ��¡Զ�ֿ̲Ⲣָ���ֿ���
git clone repository��ַ �ֿ���

# ��Զ�ֿ̲��뱾�زֿ⽨������
git remote add orgin Զ�ֿ̲��ַ

# ����ָ���ļ����ݴ���
git add �ļ�ȫ��
# �����޸ĵ��ݴ���(���������ļ�, ɾ���ļ�, �޸��ļ�)
git add .

# �ύ���浽�ݴ������޸�
git commit -m "�ύ˵��"

# ���ύ���ݴ������޸���������
git stash save "�ݴ���"
# �������µ������ݴ�, ��ɾ��
git stash apply
# �鿴���е�stash
git stash list
# �ָ�ָ�����ݴ�, ��ɾ��
git stash apply �ݴ���

# �ο��ֿ��ύ��¼
git log
# �鿴�ֿ���ʷ�汾��Ϣ
git reflog
# ���˵�ָ���汾
git reset commit-id
# ���˵�ָ���汾, �޸��ƶ����ݴ���
git reset --soft HEAD~1
# ���˵�ָ���汾, ���������޸Ļ����
git reset --hard HEAD~1
# ��ָ���ļ����ݴ������˵�������
git reset HEAD �ļ���
# ��git���˵���ʷ�汾�������ύһ��
git revert commit-id

# ������֧
git branch ��֧��
# �л���֧
git checkout ��֧��
# ���˹��������ļ��޸�
git checkout �ļ���
# ���˹�������ȫ���ļ��޸�
git checkout --hard HEAD
# �������ط�֧����Զ�̷�֧������ϵ
git checkout -b ��֧���� Զ�̷�֧����
# �鿴���ط�֧��Զ�̷�֧��ӳ���ϵ
git branch -vv
# �鿴���з�֧
git branch --list
# ɾ����֧
git branch -d ��֧����
# ɾ����֧(��������û��merge)
git branch -D ��֧����
# ��ָ����֧�ϲ�����ǰ��֧
git merge ��֧��
# ��Զ�ֿ̲���ºϲ�����ǰ��֧
git merge FETCH_HEAD
# ��ָ����֧�ϲ�����ǰ��֧
git rebase ��֧��

# ��ȡԶ�̷�֧�뱾�ط�֧���кϲ�
git pull orgin Զ�̷�֧��:���ط�֧��

# ����ǰ��֧�޸����͵�Զ�̷�֧
git push origin ���ط�֧��:Զ�̷�֧��

# �鿴���з�֧
git branch -a
# ��Զ�ֿ̲��ϵ����и�����ȡ������
git fetch Զ��������
# ��Զ�ֿ̲�ָ���ķ�֧���µ�����
git fetch Զ�������� Զ�̷�֧��
# �ϲ���ȡ�����·�֧
git merge FETCH_HEAD

# ����ǰ��֧����׷�ٹ�ϵ
git branch --set-upstream-to origin/master

# ********************
# �ܽ�����ύ����
# 1. �������޸��ύ���ݴ���
git add .
# 2. ���ݴ����޸�����
git stash save "�ݴ���"
# 3. ��Զ�ֿ̲������ύ��ȡ������
git fetch orgin master
# 4. ��Զ�ֿ̲���ºϲ�������, ������ͻ�����ͻ
git merge FETCH_HEAD
# 5. �������µ������ݴ�, ������ͻ�����ͻ
git stash apply �ݴ���
# 6. ���޸������ύ
git commit -m "�ύ˵��"
# 6. �����زֿ��޸�ͬ����Զ�ֿ̲�, ������ͻ, �����ͻ���ύ��ͬ��
git push origin ���ط�֧��:Զ�̷�֧��


