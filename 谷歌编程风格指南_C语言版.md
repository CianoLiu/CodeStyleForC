
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

### 1. ͨ����������
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
�ļ���Ҫȫ��Сд�����԰����»��ߣ�\_������ߣ�-��������ĿԼ���������û�еĻ������"\_"��
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
������һ��Сд�����ʼ����»�����������ĳ�Ա�������»��߽�β����my\_exciting\_local_variable�� my\_exciting\_member\_variable\_��  

**��ͨ����������**  
������  

	string table_name; // OK - uses underscore.
	string tablename; // OK - all lowercase.
	string tableName; // Bad - mixed case.
	
**ȫ�ֱ�����**  
��ȫ�ֱ���û���ر�Ҫ�����þͺã�������g_����������ֲ��������ֵı�־Ϊǰ׺��

### 5. ��������
������ǰ��k�� kDaysInAWeek��  
���б���ʱ�����������Ǿֲ��ġ�ȫ�ֵĻ������еģ���������������Щ������k��Ӵ�д��ĸ��ͷ�ĵ��ʣ�  

	const int kDaysInAWeek = 7
	
### 6. ��������  

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

### 8. ������

�㲢������ʹ�ú꣬�԰ɣ����ʹ�ã��������� 'MY_MACRO_THAT_SCARES_SMALL_CHILDREN��'  
�ο�����ƪԤ����꣬ ͨ���ǲ�ʹ�ú�ģ� �������Ҫ�ã� ��������ö������һ��ȫ����д��
ʹ���»��ߣ�  

	#define ROUND(x) ...
	#define PI_ROUNDED 3.0

	
## �ˡ�ע��


ע����Ȼд������ʹ�࣬���Ա�֤����ɶ�����Ϊ��Ҫ������Ĺ���������Ӧ��ע��ʲô��ע�����Ķ�����ȻҲҪ��ס��ע�͵�ȷ����Ҫ������õĴ��뱾������ĵ��� selfdocumenting�� �����ͺͱ�������������ȷҪ��ͨ��ע�ͽ���ģ���������õöࡣע����Ϊ���� ����һ����Ҫ�����Ĵ�����ˣ� ��д�ģ� �����ɣ� ����һ���˿��ܾ����㣡

### 1. ע�ͷ��

ʹ��//��/* */��ͳһ�ͺá�

//��/* */�����ԣ� //ֻ���õĸ��ӹ㷺�������ע�ͺ�ע�ͷ����ȷ��ͳһ��


### 2. �ļ�ע��

��ÿһ���ļ���ͷ�����Ȩ���档  

�ļ�ע���������ļ������ݡ��������е��ļ���Ӧ��Ҫ���ļ�ע�ͣ�  

#### ��ɺ�����

ÿ���ļ���Ӧ�������֤��Ϊ��Ŀѡ����ʵ����֤�汾����Apache 2.0��BSD�� LGPL�� GPL��
�����Ϊһ���ļ������޴�ı䣬���Լ����Լ����֡�

#### �ļ����ݣ�  

ͨ����.h�ļ�Ҫ������������Ĺ��ܺ��÷�����˵����.cc�ļ������˸����ʵ��ϸ�ڻ��㷨���ۣ������о���Щʵ��ϸ�ڻ��㷨���۶����Ķ��а��������԰�.cc�е�ע�ͷŵ�.h�У�����.cc��ָ���ĵ���.h�С�

��Ҫ������.h��.cc�临��ע�ͣ����Ƶ�ע��ƫ����ʵ�����塣


### 3. ����ע��

**����������**
ע��������֮ǰ�������������ܼ��÷���ע��ʹ������ʽ�� "Opens the file"������ָ��ʽ�� "Open the file"����ע��ֻ��Ϊ���������������Ǹ��ߺ�����ʲô��ͨ����ע�Ͳ��������������ʵ�֣����Ƕ��岿�ֵ����顣   

����������ע�͵����ݣ�  
1) inputs�����룩 �� outputs������� ��  
2) �����Ա�������ԣ����������ڼ�����Ƿ���Ҫ�������ò������Ƿ���ͷ���Щ������  
3) ������������˿ռ䣬��Ҫ�ɵ������ͷţ�  
4) �����Ƿ����ΪNULL��  
5) �Ƿ���ں���ʹ�õ��������ǣ� performance implications�� ��  
6) ��������ǿ�����ģ� re-entrant�� ����ͬ��ǰ�ᣨ synchronization assumptions����ʲô��  

�������£�  

	// Returns an iterator for this table.  It is the client's
	// responsibility to delete the iterator when it is done with it,
	// and it must not use the iterator once the GargantuanTable object
	// on which the iterator was created has been deleted.
	//
	// The iterator is initially positioned at the beginning of the table.
	//
	// This method is equivalent to:
	//    Iterator* iter = table->NewIterator();
	//    iter->Seek("");
	//    return iter;
	// If you are going to immediately seek to another place in the
	// returned iterator, it will be faster to use NewIterator()
	// and avoid the extra seek.
	Iterator* GetIterator() const;
	
����Ҫ����ν������Զ��׼���ע�ͣ������ע�;�û�б�Ҫ���ϡ�returns false otherwise������Ϊ�Ѿ����������ˣ�  

	// Returns true if the table cannot hold any more entries.
	bool IsTableFull();


**�������壺**  

ÿ����������ʱҪ��ע��˵���������ܺ�ʵ��Ҫ�㣬��ʹ�õ�Ư�����롢ʵ�ֵļ�Ҫ���衢���ʵ�ֵ����ɡ�Ϊʲôǰ�벿��Ҫ��������벿�ֲ���Ҫ����Ҫ��.h�ļ��������ط��ĺ���������ֱ�Ӹ���ע�ͣ���Ҫ˵�����������ǿ��Եģ����ص�Ҫ�������ʵ���ϡ�  

### 4. ����ע��   

ͨ���������������Ժܺ�˵��������;���ض�����£���Ҫ����ע��˵����  

**ȫ�ֱ�������������**  

�����ݳ�Ա���ƣ�����ȫ�ֱ�����������ҲӦע��˵�����弰��;���磺

	// The total number of tests cases that we run through in this regression test.
	const int kNumTestCases = 6;
	
### 6. ʵ��ע��
����ʵ�ִ���������ġ���ɬ�ġ���Ȥ�ġ���Ҫ�ĵط�����ע�͡�  

**����ǰע�ͣ�**  

���ʵĻ��ӵĴ����ǰҪ��ע�ͣ��磺

	// Divide result by two, taking into account that x
	// contains the carry from the add.
	for (int i = 0; i < result->size(); i++) {
	x
	= (x << 8) + (*result)[i];
	(*result)[i] = x >> 1;
	x &= 1;
	}
	
**��ע�ͣ�**  

�Ƚ����޵ĵط�Ҫ����β����ע�ͣ������ڴ���֮����������βע�ͣ��磺  

	// If we have enough memory, mmap the data portion too.
	mmap_budget = max<int64>(0, mmap_budget - index_->length());
	if (mmap_budget >= data_size_ && !MmapData(mmap_chunk_bytes, mlock))
	  return;  // Error already logged.

ע�⣬������ע��������δ��룬����������ʱע���ἰ�����Ѿ���������־��  
ǰ�����ڼ��ж���ע�ͣ������ʵ�����ʹ֮�ɶ��Ը��ã�  

	DoSomething();                  // Comment here so the comments line up.
	DoSomethingElseThatIsLonger();  // Two spaces between the code and the comment.
	{ // One space before comment when opening a new scope is allowed,
	  // thus the comment lines up with the following comments and code.
	  DoSomethingElse();  // Two spaces before line comments normally.
	}
	vector<string> list{// Comments in braced lists describe the next element ..
						"First item",
						// .. and should be aligned appropriately.
						"Second item"};
	DoSomething(); /* For trailing block comments, one space is fine. */


### 7. ��㡢ƴд���﷨

�����㡢ƴд���﷨��д�ĺõ�ע�ͱȲ��Ҫ�׶��Ķࡣ  

ע��һ���ǰ����ʵ���д�;�㣨 .���������ľ��ӣ���һ���ע�ͣ��������β��ע�ͣ���������㣬 ��ȻҪע�����һ���ԡ� �����ľ��ӿɶ��Ը��ã� Ҳ����˵����ע���������Ķ�����һ�㲻������뷨��  

��Ȼ������ָ�����÷ֺţ� semicolon�� ��ʱ�����˶��ţ� comma�� �е����Ρ������׶��Ĵ��뻹�Ǻ���Ҫ�ģ��ʵ��ı�㡢ƴд���﷨�Դ˻�����������

### 8. TODOע��

����Щ��ʱ�ġ����ڵĽ�����������Ѿ����õ����������Ĵ���ʹ��TODOע�͡�  

������ע��Ҫʹ��ȫ��д���ַ���TODO���������ţ� parentheses�� �������Ĵ������ʼ���ַ�ȣ������Լ���ð�ţ� colon����Ŀ���ǿ��Ը���ͳһ��TODO��ʽ���в��ң�

	// TODO(kl@gmail.com): Use a "*" here for concatenation operator.
	// TODO(Zeke) change this to use relations.
	// TODO(bug 12345): remove the "Last visitors" feature

���������Ϊ���ڡ�����ĳһ����ĳ�¡������Լ���һ���ض���ʱ�䣨 "Fix by November 2005"�����¼��� "Remove this code when all clients can handle XML
responses."����

## �š���ʽ

������͸�ʽȷʵ�Ƚ����⣬��һ����Ŀ����������ѭͬһ����Ƿǳ����׵ģ���Ϊ����δ��ͬ��������ʽ�����ÿһ������������Ŀ����ͳһ�ı�̷���Ǻ���Ҫ�ģ����������������������Ķ���������ʱ�������ס�  

### 1. �г���

ÿһ�д����ַ���������80��

����Ҳ��ʶ�����������Ǵ�������ģ�����˶�Ĵ��붼������һ�������Ǹо�һ���Ը���Ҫ��

�ŵ㣺 
�ᳫ��ԭ�������Ϊǿ�����ǵ����༭�����ڴ�С��Ұ�����ܶ���ͬʱ���ſ��������ڣ�����û�ж���ռ��ؿ�ĳ�����ڣ����ǽ��������ߴ�����޶���һ��ʹ��80�п�ΪʲôҪ�ı��أ�

ȱ�㣺
���Ը�ԭ���������Ϊ����Ĵ����и����Ķ���80�е��������ϸ�����60����Ĵ��ͻ��ĹŰ�ȱ�ݣ��ִ��豸���и������ʾ���������ɵĿ�����ʾ������롣

���ۣ� 
80���ַ������ֵ��

���⣺
1) ���һ��ע�Ͱ����˳���80�ַ��������URL�����ڸ���ճ���ķ�����Գ���80�ַ���
2) ������·���Ŀ��Գ���80�У��������⣻
3) ͷ�ļ���������ֹ�ظ��������������Ӹ�ԭ��

### 2. ��ASCII�ַ�  

������ʹ�÷�ASCII�ַ���ʹ��ʱ����ʹ�� UTF-8��ʽ��  

������Ӣ�ģ�Ҳ��Ӧ���û�������ı�Ӳ���뵽Դ�����У���˷�ASCII�ַ�Ҫ���á���������¿����ʵ����������ַ����磬��������ⲿ�����ļ�ʱ�������ʵ�Ӳ���������ļ�����Ϊ�ָ����ķ�ASCII�ַ����������õ��ǣ�����Ҫ���ػ��ģ���Ԫ���Դ�����ܰ�����ASCII�ַ�������������£�Ӧʹ��UTF-8��ʽ����Ϊ�ܶ๤�߶��������ʹ�������룬 ʮ�����Ʊ���Ҳ���ԣ� ����������ǿ�ɶ��Ե�����¡�����"\xEF\xBB\xBF"��Unicode��zero-width no-break space�ַ�����UTF-8��ʽ������Դ�ļ����ǲ��ɼ��ġ�


### 3. �ո��Tabs

ֻʹ�ÿո�ÿ������2���ո�  

ʹ�ÿո������������Ҫ�ڴ�����ʹ��tabs���趨�༭����tabתΪ�ո�  

### 4. ���������붨��

�������ͺͺ�������ͬһ�У����ʵĻ�������Ҳ����ͬһ�С�
��������ȥ��������  

	ReturnType ClassName::FunctionName(Type par_name1, Type par_name2) {
	  DoSomething();
	  ...
	}
	
���ͬһ���ı��϶࣬�ݲ������в�����  

	ReturnType ClassName::ReallyLongFunctionName(Type par_name1, Type par_name2,
												 Type par_name3) {
	  DoSomething();
	  ...
	}
	
��������һ���������Ų��£�  

	ReturnType LongClassName::ReallyReallyReallyLongFunctionName(
	    Type par_name1,  // 4 space indent
	    Type par_name2,
	    Type par_name3) {
	  DoSomething();  // 2 space indent
	  ...
	}
	
ע�����¼��㣺

- ѡ��õĲ������֡�  
- �������û�õĻ������������Բ�Ҫ��  
- ����ֵ���Ǻͺ�������ͬһ�С�  
- ���������Ͷ���ķ������͵ĵط���Ҫ���ո�  
- ��Բ���ţ�open parenthesis�� ���Ǻͺ�������ͬһ�С�  
- ����������Բ���ż�û�пո�  
- Բ�����������û�пո�  
- ������ţ�open curly brace�� �������һ������ͬһ�е�ĩβ���������µ�һ�С�  
- �Ҵ����ţ�close curly brace�� ���ǵ���λ�ں������һ�С�  
- ��Բ���ţ�close parenthesis�� ��������ż�������һ���ո�  
- �����β�Ӧ�����ܶ��롣  
- ȱʡ����Ϊ2���ո�  
- ������װ�Ĳ�������4���ո��������  


	class Foo {
	 public:
	  Foo(Foo&&);
	  Foo(const Foo&);
	  Foo& operator=(Foo&&);
	  Foo& operator=(const Foo&);
	};

	class Shape {
	 public:
	  virtual void Rotate(double radians) = 0;
	};

	class Circle : public Shape {
	 public:
	  void Rotate(double radians) override;
	};

	void Circle::Rotate(double /*radians*/) {}
	// Bad - if someone wants to implement later, it's not clear what the
	// variable means.
	void Circle::Rotate(double) {}


Attributes, and macros that expand to attributes, appear at the very beginning of the function declaration or definition, before the return type:

	MUST_USE_RESULT bool IsOK();

### 5. ��������

��������ͬһ�У����򣬽�ʵ�η�װ��Բ�����С�
����������ѭ������ʽ��

	bool result = DoSomething(argument1, argument2, argument3);
	
���ͬһ�зŲ��£��ɶ�Ϊ���У�����ÿһ�ж��͵�һ��ʵ�ζ��룬��Բ���ź����Բ����ǰ��Ҫ���ո�

	bool result = DoSomething(averyveryveryverylongargument1,
                              argument2, argument3);
	
����Ҳ���Խ��溯������֮��4���ո�������  

	if (...) {
	  ...
	  ...
	  if (...) {
		bool result = DoSomething(
			argument1, argument2,  // 4 space indent
			argument3, argument4);
		...
	  }
	  
��ʱΪ�˿ɶ��ԣ�Ҳ���������Ű棺

	// Transform the widget by a 3x3 matrix.
	my_widget.Transform(x1, x2, x3,
						y1, y2, y3,
						z1, z2, z3);

### 6. �������

�ᳫ����Բ��������ӿո񣬹ؼ���else����һ�С�  

�Ի���������������ֿ��Խ��ܵĸ�ʽ��һ����Բ���ź�����֮���пո�һ��û�С�

�������û�пո�ĸ�ʽ�����ֶ����ԣ�����һ����Ϊ��������������޸�һ���ļ����ο���ǰ���и�ʽ�������д�µĴ��룬�ο�Ŀ¼�»���Ŀ�������ļ��ĸ�ʽ�������ǻ��Ļ����Ͳ�Ҫ�ӿո��ˡ�

	if (condition) { // no spaces inside parentheses
	... // 2 space indent.
	} else { // The else goes on the same line as the closing brace.
	...
	}
	
�������������Բ�����ڲ��ӿո�  

	if ( condition ) { // spaces inside parentheses - rare
	... // 2 space indent.
	} else { // The else goes on the same line as the closing brace.
	...
	}

ע�����������if����Բ���ż��и��ո���Բ���ź�������ţ����ʹ�õĻ�����ҲҪ�и��ո�  

	if(condition) // Bad - space missing after IF.
	if (condition){ // Bad - space missing before {.
	if(condition){ // Doubly bad.
	
	if (condition) { // Good - proper space after IF and before {.

��Щ�������д��ͬһ������ǿ�ɶ��ԣ�ֻ�е����򵥲���û��ʹ��else�Ӿ�ʱʹ�ã�

	if (x == kFoo) return new Foo();
	if (x == kBar) return new Bar();

��������else��֧�ǲ�����ģ�  

	// Not allowed - IF statement on one line when there is an ELSE clause
	if (x) DoThis();
	else DoThat();
	
ͨ����������䲻��Ҫʹ�ô����ţ������ϲ��Ҳ�޿ɺ�ǣ�Ҳ����Ҫ��if����ʹ�ô����ţ�

	if (condition)
	  DoSomething(); // 2 space indent.
	  
	if (condition) {
	  DoSomething(); // 2 space indent.
	}
	
������������һ��֧ʹ���˴����ŵĻ�����������Ҳ����ʹ�ã�  

	// Not allowed - curly on IF but not ELSE
	if (condition) {
	  foo;
	} else
	  bar;
	  
	// Not allowed - curly on ELSE but not IF
	if (condition)
	  foo;
	else {
	  bar;
	}

	// Curly braces around both IF and ELSE required because
	// one of the clauses used braces.
	if (condition) {
	  foo;
	} else {
	  bar;
	}

	
### 7. ѭ����switchѡ�����

switch������ʹ�ô����ŷֿ飻��ѭ����Ӧʹ��{}��continue��

switch����е�case�����ʹ�ô�����Ҳ���Բ��ã�ȡ�������ϲ�ã�ʹ��ʱҪ������������

����в�����caseö��������ֵ��Ҫ���ǰ���һ��default�����������ֵû��caseȥ�����������������������default������ִ�У����Լ򵥵�ʹ��assert��

	switch (var) {
	  case 0: {  // 2 space indent
		...      // 4 space indent
		break;
	  }
	  case 1: {
		...
		break;
	  }
	  default: {
		assert(false);
	  }
	}
	
����������ѭ�����У������ǿ�ѡ�ġ�

	for (int i = 0; i < kSomeNumber; ++i)
	  printf("I love you\n");

	for (int i = 0; i < kSomeNumber; ++i) {
	  printf("I take it back\n");
	}

��ѭ����Ҫ�����Ż���continue��������ֱ���ø��ֺš�

	while (condition) {
	  // Repeat test until it returns false.
	}
	for (int i = 0; i < kSomeNumber; ++i) {}  // Good - empty body.
	while (condition) continue;  // Good - continue indicates no logic.

	while (condition);  // Bad - looks like part of do/while loop.


### 8. ָ������ñ��ʽ

��ͷ��->��ǰ��Ҫ�пո�ָ��/��ַ��������*��&����Ҫ�пո�

������ָ������ñ��ʽ����ȷ������

	x = *p;
	p = &x;
	x = r->y;
	
ע�⣺  

- �ڷ��ʳ�Աʱ����ͷǰ��û�пո�
- ָ�������*��&��û�пո�  

������ָ����������ʱ���Ǻ������ͻ���������������ԣ�

	// These are fine, space preceding.
	char *c;
	const string &str;
	
	// These are fine, space following.
	char* c; // but remember to do "char* c, *d, *e, ...;"!
	const string& str;
	
	char * c; // Bad - spaces on both sides of *
	const string & str; // Bad - spaces on both sides of &
	
ͬһ���ļ����½������У�������Ҫ����һ�¡�

### 9. �������ʽ  

���һ���������ʽ������׼�п�0�ַ������������Ҫͳһһ�¡�
�����У��߼��루&&����������λ����β��

	if (this_one_thing > this_other_thing &&
	    a_third_thing == a_fourth_thing &&
	    yet_another & last_one) {
	  ...
	}
	
�����߼��루&&����������λ����β�����Կ��Ƕ������Բ���ţ�����ʹ�õĻ�����ǿ�ɶ����Ǻ��а����ġ�

### 10. ����ֵ

return���ʽ�в�Ҫʹ��Բ���š�

	return result;                  // No parentheses in the simple case.
	// Parentheses OK to make a complex expression more readable.
	return (some_long_condition &&
			another_condition);
			
	return (value);                // You wouldn't write var = (value);
	return(result);                // return is not a function!

	
### 11. �����������ʼ��

ѡ��=����()��
��Ҫ������֮������ѡ���������ʽ������ȷ�ģ�

	int x = 3;
	int x(3);
	string name("Some Name");
	string name = "Some Name"
	
### 12. Ԥ����ָ��

Ԥ����ָ�Ҫ�����������׿�ʼ��
��ʹԤ����ָ��λ������������У�ָ��ҲӦ�����׿�ʼ��

	// Good - directives at beginning of line
	  if (lopsided_score) {
	#if DISASTER_PENDING      // Correct -- Starts at beginning of line
		DropEverything();
	# if NOTIFY               // OK but not required -- Spaces after #
		NotifyClient();
	# endif
	#endif
		BackToNormal();
	  }
	  
	// Bad - indented directives
	  if (lopsided_score) {
		#if DISASTER_PENDING  // Wrong!  The "#if" should be at beginning of line
		DropEverything();
		#endif                // Wrong!  Do not indent "#endif"
		BackToNormal();
	  }	  

  
### 13. ˮƽ����
ˮƽ���׵�ʹ��������ˡ���Ҫ����β�����ν�����ס�

#### ͨ����  

	void f(bool b) {  // Open braces should always have a space before them.
	  ...
	int i = 0;  // Semicolons usually have no space before them.
	// Spaces inside braces for braced-init-list are optional.  If you use them,
	// put them on both sides!
	int x[] = { 0 };
	int x[] = {0};

�����������׻�������˱༭ʱ��ɶ��⸺�������������Ǻϲ������ʱ�򣬼�ʹ���ǿ���ȥ��������ո���ˣ���Ҫ�������Ŀո�����㲻С�������˶���Ŀո�Ҫ����ȥ����������ר������ո�ʱȥ����ȷ��û��������ͬʱ��ʹ�ø��ļ�����

#### ѭ���ʹ�ֱ���ף�  

	if (b) {          // Space after the keyword in conditions and loops.
	} else {          // Spaces around else.
	}
	while (test) {}   // There is usually no space inside parentheses.
	switch (i) {
	for (int i = 0; i < 5; ++i) {
	// Loops and conditions may have spaces inside parentheses, but this
	// is rare.  Be consistent.
	switch ( i ) {
	if ( test ) {
	for ( int i = 0; i < 5; ++i ) {
	// For loops always have a space after the semicolon.  They may have a space
	// before the semicolon, but this is rare.
	for ( ; i < 5 ; ++i) {
	  ...

	// Range-based for loops always have a space before and after the colon.
	for (auto x : counts) {
	  ...
	}
	switch (i) {
	  case 1:         // No space before colon in a switch case.
		...
	  case 2: break;  // Use a space after a colon if there's code after it.

#### ��������  

	// Assignment operators always have spaces around them.
	x = 0;

	// Other binary operators usually have spaces around them, but it's
	// OK to remove spaces around factors.  Parentheses should have no
	// internal padding.
	v = w * x + y / z;
	v = w*x + y/z;
	v = w * (x + z);

	// No spaces separating unary operators and their arguments.
	x = -5;
	++x;
	if (x && !y)
	  ...
  
### 14. ��ֱ����
��ֱ����Խ��Խ�á�

�ⲻ�����ǹ������ԭ�������ˣ����Ƿǳ��б�Ҫ�Ļ��Ͳ�Ҫʹ�ÿ��С������ǣ���Ҫ��������������֮��ճ���2�У�������ͷ��β��Ҫ�п��У���������Ҳ��Ҫ������ӿ��С�

����ԭ���ǣ�ͬһ��������ʾԽ��Ĵ��룬����Ŀ�������Խ������⡣��Ȼ�������ܼ��Ĵ����͹������ɵĴ����ͬ���ѿ���ȡ��������жϣ���ͨ����Խ��Խ�á�

һЩ���ڿ��еľ���Ҳ�����ã�
- ������ʼ�ͽ����Ļ��жԿɶ��Ի���ûʲô������
- ��������if-else�������еĿ���Ҳ�����ô�����пɶ��ԡ�

