
## һ��ͷ�ļ�

ͨ����ÿһ��.cc�ļ��� C++��Դ�ļ�������һ����Ӧ��.h�ļ���ͷ�ļ�����Ҳ��һЩ���⣬�絥Ԫ���Դ����ֻ����main()��.cc�ļ���
��ȷʹ��ͷ�ļ���������ڿɶ��ԡ��ļ���С�������ϴ�Ϊ�Ĺۡ�
����Ĺ�����������ʹ��ͷ�ļ�ʱ�ĸ����鷳��

### 1.�԰���ͷ�ļ�(�о��ⲿ�ֵúú������£�Ŀǰû˼·)

ͷ�ļ�Ӧ���԰���(������Ҫ���������Լ�)���Լ���.h��β����ͷ�ļ���Ҫ�������Ļ���Ӧ����.inc��β��

���е�ͷ�ļ���Ӧ���԰������û����ع����߲�Ӧ�������������ȥ����ͷ�ļ����ر�أ�һ��ͷ�ļ�Ӧ����ͷ����������������Ҫ������ͷ�ļ���

���һ��ģ���������������.h�ļ���������������ͬ��ͷ�ļ��ͻ��ṩ���Ķ��塣��Щ����ᱻ������ʹ������.c�ļ��У��������ͻ�����ʧ�ܡ���Ҫ�Ѷ���ֿ���

### 2.#define�ı���

����ͷ�ļ���Ӧ��ʹ��#define��ֹͷ�ļ������ذ����� multipleinclusion�� ��������ʽӦ���ǣ�<PROJECT>_<PATH>_<FILE>_H_

Ϊ��֤Ψһ�ԣ�ͷ�ļ�������Ӧ����������ĿԴ������ȫ·�������磬��Ŀfoo�е�ͷ�ļ�foo/src/bar/baz.h��Ӧ�ð����·�ʽ������

	#ifndef FOO_BAR_BAZ_H_
	#define FOO_BAR_BAZ_H_
	...
	#endif //FOO_BAR_BAZ_H_
	
	
### 3. ǰ������(C++ר��)

### 4. ��������(C++ר��)

### 5. -inl.h�ļ�(C++ר��)

### 6. �����ļ������Ƽ�����
�����������׼������ǿ�ɶ��ԡ����������������������£�����ͷ�ļ���C�⡢C++�⡢�������.h����Ŀ�ڵ�.h��

��Ŀ��ͷ�ļ�Ӧ������ĿԴ����Ŀ¼���ṹ���У����ұ���ʹ��UNIX�ļ�·��.����ǰĿ¼����..����Ŀ¼�������磬 google-awesome-project/src/base/logging.hӦ��������������

	#include "base/logging.h"
	
dir/foo.cc ����Ҫ������ִ�л����dir2/foo2.h�Ĺ��ܣ�foo.cc�а���ͷ�ļ��Ĵ������£�

	1.dir2/foo2.h
	2.Cϵͳ�ļ�
	3.C++ϵͳ�ļ�
	4.������ͷ�ļ�
	5.����Ŀ��ͷ�ļ�
	
��������ʽ����Ч����������������� dir2/foo2.h ��©���κα�Ҫ�İ������Ǳ��� dir/foo.cc ʱ�ͻ��жϡ��������֤�˱����жϻ����ȳ�������Щ����ǰ�ļ�������ǰ�������Ǳ�İ��е��޹ص��ˡ�

dir/foo.cc��dir2/foo2.hͨ��λ����ͬĿ¼�£��� base/basictypes_unittest.cc�� base/basictypes.h������Ҳ���ڲ�ͬĿ¼�¡�

��ͬĿ¼��ͷ�ļ�����ĸ���ǲ����ѡ��

������˵��google-awesome-project/src/foo/internal/fooserver.cc�İ����������£�


	#include "foo/public/fooserver.h"

	#include <sys/types.h>
	#include <unistd.h>

	#include <hash_map>
	#include <vector>

	#include "base/basictypes.h"
	#include "base/commandlineflags.h"
	#include "foo/public/bar.h



## ����������

������Ⱦ�����ڴ󲿷���C++��֪ʶ������C�����Խ������������ʡ�������Ⱦ��������ģ���ڲ��ı�������ýṹ������������ֹ��Ⱦ��

## ������

## �ġ�����
### 1. ����˳��

### 2. ��д��С����
��סһ�㣬��д��С������

## �塢Google���еķ���

## ��������C++����

### sizeof
��������sizeof(varname)����sizeof(type)��
ʹ��sizeof(varname)����Ϊ���������͸ı�ʱ�����Զ�ͬ������Щ�����sizeof(type)���������壬����Ҫ�������⣬����������͸ı�Ļ�����ͬ����

	Struct data;
	memset(&data, 0, sizeof(data));
	memset(&data, 0, sizeof(Struct));// ���õķ�ʽ

## �ߡ�����
��Ҫ��һ���Թ��������������������ֱ�ӿ���ֱ��ȷ������ʵ���ǣ����͡���������������������ȵȣ��������ʵ�����������Ǵ����е�ģʽƥ��������������Щ�������������������һ�������ԣ�����Ȱ�����ϲ��������һ���Ը���Ҫ�����Բ�������ô�룬�����ܹ��ǹ���

### 1. ͨ���������� General Naming Rules��
���������������������ļ�����Ӧ���������ԣ���Ҫ������д��
�����ܸ������������ƣ���Ҫ��Լ�ռ䣬�ñ��˺ܿ������Ĵ������Ҫ����Ҫʹ��ģ������д��������ַ���
	int price_count_reader;    // No abbreviation.
	int num_errors;            // "num" is a widespread convention.
	int num_dns_connections;   // Most people know what "DNS" stands for.


	int n;                     // Meaningless.
	int nerr;                  // Ambiguous abbreviation.
	int n_comp_conns;          // Ambiguous abbreviation.
	int wgc_connections;       // Only your group knows what this stands for.
	int pc_reader;             // Lots of things can be abbreviated "pc".
	int cstmr_id;              // Deletes internal letters.

### 2. �ļ�����
�ļ���Ҫȫ��Сд�����԰����»��ߣ�_������ߣ�-��������ĿԼ���������û�еĻ������"_"��
�ɽ��ܵ��ļ�����:  
- my_useful_class.cc
- my-useful-class.cc
- myusefulclass.cc
- myusefulclass_test.cc // _unittest and _regtest are deprecated.

C++�ļ���.cc��β��ͷ�ļ���.h��β��
��Ҫʹ���Ѿ�������/usr/include�µ��ļ�������db.h��
ͨ�����������ļ���������ȷ��http_server_logs.h�ͱ�logs.hҪ�ã�������ʱ�ļ���һ��ɶԳ��֣���foo_bar.h��foo_bar.cc����Ӧ��FooBar��


### 3. ��������
��������ÿ�������Դ�д��ĸ��ͷ���������»��ߣ� MyExcitingClass�� MyExcitingEnum��
�����������������ࡢ�ṹ�塢���Ͷ��壨 typedef����ö�١���ʹ����ͬԼ�������磺

	// classes and structs
	class UrlTable { ...
	class UrlTableTester { ...
	struct UrlTableProperties { ...
	
	// typedefs
	typedef hash_map<UrlTableProperties *, string> PropertiesMap;
	
	// enums
	enum UrlTableErrors { ..
	
	
### 4. ��������
������һ��Сд�����ʼ����»�����������ĳ�Ա�������»��߽�β����my_exciting_local_variable�� my_exciting_member_variable_��

**��ͨ����������**
������
	string table_name; // OK - uses underscore.
	string tablename; // OK - all lowercase.
	string tableName; // Bad - mixed case.
	
**ȫ�ֱ�����**
��ȫ�ֱ���û���ر�Ҫ�����þͺã�������g_����������ֲ��������ֵı�־Ϊǰ׺��

### 5. ��������
������ǰ��k�� kDaysInAWeek��
���б���ʱ�����������Ǿֲ��ġ�ȫ�ֵĻ������еģ���������������Щ������ k��Ӵ�д��ĸ��ͷ�ĵ��ʣ�
	const int kDaysInAWeek = 7
	
### 6. ��������  
��ͨ������Сд��ϣ���ȡ������Ҫ���������ƥ�䣺 MyExcitingFunction()��MyExcitingMethod()�� my_exciting_member_variable()��set_my_exciting_member_variable()��

��ͨ������
�������Դ�д��ĸ��ͷ��ÿ����������ĸ��д(���Ǵ��շ����������߽���˹��������)�����ʼ�û���»��ߡ�����д�д��ĸ��д�ʣ������ڰ�������������(���� StartRpc()������ StartRPC())��

	AddTableEntry()
	DeleteUrl()
	OpenFileOrDie()
	
### 7. ö������

ö��ֵ��������������Ҳ�������������kEnumName ���� ENUM_NAME��
����ö��ֵ������������������������Ҳ�������������������UrlTableErrors������ö�������������ͣ���˴�Сд��ϡ�

	enum UrlTableErrors {
		kOK = 0,
		kErrorOutOfMemory,
		kErrorMalformedInput,
	};
	enum AlternateUrlTableErrors {
		OK = 0,
		OUT_OF_MEMORY = 1,
		MALFORMED_INPUT = 2,
	};

��2009��1��֮ǰ��ö��ֵ�ķ�񶼺ͺ�һ���������Ƚ����׵���������ͻ����˸�Ϊ�Ƽ�����ö���������������ԵĻ����´��뾡��ʹ�ó��������������û��Ҫȥ���ϴ��붼��Ϊ������񣬳��������˱������





