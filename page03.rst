DataFrame
========================================
DataFrame��һ�����Ʊ������ݽṹ��������������������������������һ��������У�ÿ�п����ǲ�ͬ��ֵ���ͣ���ֵ���ַ���������ֵ�ȣ���
���£�

index����������

columns����������

values��ֵ�Ķ�ά���顣

name�����֡�


����������DataFrame(sequence)��ͨ�����й����������е�ÿ��Ԫ����һ���ֵ䡣

frame=DateFrame������֮�󣬼���frame���С�name��,��age��,��addr���������ԣ�����ʹ��fame[��name��]�鿴���������ݣ�Ҳ����fame.name����ֱ�Ӳ鿴��

frame���ա�������ȡ������ÿ������һ��Series�ࡣ

DataFrame�����ʹ�ò�����������

groupby(str|array��)����������ʹ��frame�ж�Ӧ���Ե�str���ߺ�frame������ͬ��array��Ϊ����������ʹ��һ���᷵�غ�frame������ͬlist�ĺ�����Ϊ���������ʹ�ú�������������������������ĺ�������Ĳ���������fame��index�������������⡣ʹ����groupby����֮�����,size()�����Ϳ��Զ�groupby�������ͳ�ơ�

groupby�����ʹ�ã�

size()������count

sum()���������

apply(func��axis=0)���ڷ����ϵ���ʹ�ú���func����frame����groupby����DataFrame��Ĭ�Ͻ�func����ÿ�����ϣ����axis=1��ʾ��func�������ϡ�


reindex(index,column,method)���������������������Ͳ�ֵ��

size()���᷵��һ��frame�����frame��groupby��Ľ����

sum(n).argsort()�����frame�е�ֵ�����֣�����ʹ��sum��������frame���������ԣ��������ӷֱ���ͣ�������һ��Series�����Series������Ϊframe.take�Ĳ������õ�frame�ж�Ӧ���С�

pivot_table(����str1,index=str2,columns=str3,aggfunc=str4)͸��ͼ������

str1���Ǹ�����str4��Ϊ�����Ĳ��֡�

str2���Ƿ���frame��������

str3���Ƿ���frame��������

str4���Ǽ��Ϻ��������С�mean��,��sum����Щ������str2��str3���顣

ʹ��͸��ͼ����֮�󣬿���ʹ��.sum()�����ͺ�����ʹ�ú�ᰴ��index��columns�ķ�����͡�

order_index(by,ascending):
����һ������by����asceding=True��ʾ����False��ʾ�����frame

concat(list)����һ���б��frame������������

ix[index]��������������DataFrame����ͨ�±�����������

take(index)�����ú�ix��࣬���ǲ�ѯ�У�����ix�����кţ�take������������

unstack()��������Ϣ�������Ϣ��

apply(func��axis=0)��applymap(func)��apply����DataFrame��Ĭ�Ͻ�func����ÿ�����ϣ����axis=1��ʾ��func�������ϡ�applymap��ʾfunc����ÿ��Ԫ���ϡ�

combine_first(frame2)��combine_first���frame�еĿ�ֵ��frame1�ж�Ӧλ�õ����ݽ�����䡣Series����Ҳ����ͬ�ķ�����

stack()���������Խ�DataFrame����ת�����У�ԭ������������Ϊ�еĲ����������stack��unstack��������������ķ�����������������Series��DataFrame֮���ת����

duplicated()������һ��������Series����ʾ�����Ƿ��ظ���
drop_duplicates()������һ���Ƴ����ظ��к��DataFrame.
pct_change()��SeriesҲ��������������������������ͬcolnums�������ڵ�����֮��ı仯�ʡ�

corr()���������ϵ������

cov()������Э����ϵ������

corrwith(Series|list,axis=0)��axis=0ʱ����frame��ÿ�кͲ��������ϵ����
