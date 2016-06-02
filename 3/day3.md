# DAY03 #
--------------
### 1. 循环结构
- for循环和while循环，还有do while循环（必定执行一次，先执行do，在判断）
		
		do {
			sop();
			}
		while(条件); //注意次数分号
	- for循环条件表达式，必须要有真假。
	- for(初始化条件；循环条件表达式；循环后的操作方式)
	- for 不写条件表达式就默认代表真。无限循环：for(;;) while(true)
	- 累加思想与计数器思想
	- for循环嵌套
	- break 和 continue 。break作用于switch for循环。continue 作用于 for循环。
			
			w :for(int i;i<10;i++){
				q:for(....){
					.....
					break w;
					continue w;//这么写也可以
					}
				}
### 2.函数 （function）
- return; 语句结束当前函数,跟在if语句后面一般。
- 函数内部可以调用函数，不能定义函数
- 函数的重载之和参数列表有关系，**即参数个数和参数类型有关**。与函数返回值无关。函数重载一般可以嵌套。

### 3. 数组
- 格式如下：
		
		int[] a = new int[10];
		
		int[] a = new int[]{1,2,3,4};

		int[] a = {1,2,3,4};

		//int 代表数据类型，而这里的a代表数组类型的变量。引用型数据类型包括：class ,interface ,[]
- 在内存中的分配
	- java在启动时一共在内存划分五块区域。栈内存、堆内存、方法区、本地方法区、寄存器 
	- **栈内存** 用于存储局部变量，当数据使用完会**自动释放空间**，在这里赋值不影响各自的值。
	- **堆内存** 数组和对象，通过new出来的。有内存地址值，变量有默认初始化值，实体不被使用时，会被**垃圾回收**器回收。
	
			int[] a = new int[3];
			//a存放在栈内存，new 出来的对象放在堆内存中。实体的首地址赋值给a
			//默认值 int 0 ,double 0.0 ,float 0.0f ,boolean false
			//当我们不想用a的时候，指定a = null 就可以。这样以后，实体会被系统不定期回收（不一定马上执行）。java的垃圾回收机制。C++需要程序员手动清楚，而java在这里给优化了

	- 两个例子。
	
			int a = 3;
			int b = a;
			b = 5;
			sop(a) = 3 //存在于栈内存中

			-----------------------
			int[] a = new int[3];
			int[] b = a;
			a[1] = 2;
			b[1] = 4;
			sop(a[1]) = 4; //a和b都是数组类型，指向同一个引用
			

			 