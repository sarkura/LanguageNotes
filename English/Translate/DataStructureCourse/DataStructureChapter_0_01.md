---
created: {{date:2026-9-12}}
updated: {{date:2026-9-12}}
type: Translation
language: English
level: B2
status: Finished
source_lang: en-US
target_lang: zh-CN
source_type: Technology
topic: DataStructure
difficulty: Medium
tags:
  - English
  - Translation
aliases:
  - "Data Structure & Algorithm"
---

# Data Structure & Algorithm

## 1. Metadata
    Title : How data structures are stored
    Author / Source / Link : Labuladong / Data Structure & Algorithm / https://labuladong.online/en/algo/essential-technique/algorithm-summary/
    Type : Technology
    Source language : English
---

## 2. Translation

### Source

```
    There are only two ways to store data structures: arrays (stored in order) and linked lists (stored by links).
    How to understand this? Aren’t there hash tables, stacks, queues, heaps, trees, graphs, and many other data structures?
    When we analyze a problem, we should think in a recursive way: top-down, from abstract to concrete. If you list all those structures first, 
    they are higher-level designs. Arrays and linked lists are the base. All those different structures are special operations on arrays or linked lists. 
    They just have different APIs.
    For example, queues and stacks can be implemented with either a linked list or an array. With an array, you need to handle growing and shrinking. 
    With a linked list, you don’t have this problem, but you need more memory for node pointers.
    A graph has two common storage ways. An adjacency list is a linked list. An adjacency matrix is a 2D array. 
    An adjacency matrix is fast for checking connections, and you can use matrix operations to solve some problems. 
    But if the graph is sparse, it wastes a lot of space. An adjacency list saves space, but many operations are slower than an adjacency matrix.
    A hash table uses a hash function to map keys into a large array. 
    For hash collisions, separate chaining needs linked list features. It is simple, but needs extra space for pointers. 
    linear probing needs array features for continuous addressing. It does not need pointer space, but the operations are a bit more complex.
    For trees: if you use an array, it becomes a “heap”, because a heap is a complete binary tree. With an array, you don’t need node pointers, 
    and operations are simpler. A classic example is the binary heap. If you use a linked list, it is the common “tree” form. 
    Because it may not be a complete binary tree, it is not good to store it in an array. Based on this linked-list “tree”, 
    people created many designs, like binary search tree, AVL tree, red-black tree, segment tree, B-tree, and so on, for different problems.
    So there are many data structures. You can even invent your own. But at the storage level, it is still just arrays or linked lists. 
    Their pros and cons are:
    Array stores data in a tight, continuous block. You can do random access and quickly find an element by index, and it saves space. 
    But because it must be continuous, memory must be allocated in one piece. So if you need to grow the array,
     you must allocate a bigger block and copy all data, which is O(N). Also, if you insert or delete in the middle, 
     you must move all later elements to keep it continuous, which is also O(N).
    Linked list does not store elements continuously. Each node uses pointers to the next node, so there is no “grow array” problem. 
    If you know the previous and next node, you can delete or insert by changing pointers, which is O(1). 
    But because memory is not continuous, you cannot compute an element’s address from an index, so you cannot do random access. 
    Also, each element needs pointers (to previous/next), so it uses more space.
```

### Translate

```
    Self-Verson:
    只有两种方式去储存数据结构: 数组(连续储存)，链表(链接储存)。
    如何去理解这个？难道这不是哈希表，栈，队列，堆，树，图和许多其他数据结构吗？
    当我们要分析这个问题时，我们应该按照递归的思考方式: 自顶向下，从抽象到具体。如果你首先列出这些结构，那些是高级的设计结构。数组和链表才是基本结构。
    那些不同的数据结构是独特的操作下的不同数组或链表。他们仅仅拥有不同的调用接口。
    举例来说，队列和栈可以通过任意链表或者数组实现。使用数组时，你需要去控制增长空间和清除空间。使用链表时，你没有这个问题，但是你需要更多空间来存放节点指针。
    一个哈希表使用哈希函数在大数组中排列关键索引。对于哈希碰撞，分离的链式结构需要链接链表的特性。这很简单，但是需要额外的空间存放指针。线性探测法需要数组的连续地址特性。
    这不需要指针空间，但是操作上会更加复杂一些。
    对于树来说: 如果你使用数组来存放，他将变成堆结构，因为堆是一个完全二叉树。使用一个数组，你不需要节点指针和操作会更简单。一个经典的例子是二叉堆。
    如果你使用链表来存放，它是一个常见的树形结构。因为它或许不是完全二叉树，不适合用数组来存储。基于链表的树，人们创造了许多设计，
    像二叉查找树，平衡树，红黑树，线段树，B树或其他树，对于不同问题来说不一致。
    因此这是许多数据结构。你甚至可以自己发明属于自己的结构。但是在存储级别来看，它仍然仅仅只是数组或者链表。
    他们的优缺点是:
    数组的储存可以紧致，连续空间。你可以随机访问和快速按照索引查找一个元素，还有它可以节约空间。但正因为必须连续，内存申请必须在同一区域。
    所以如果你需要扩大空间，你必须申请另一块更大的连续内存，然后复制所有数据，这样会是O(N)的开销。而且，如果你在数组中间进行插入或者删除元素，
    你必须移动所有之后的元素去保持连续性，这也是O(N)的开销。
    链表不存储连续元素。每一个节点使用指针连接下一个节点，所有它没有内存增长问题。如果你知道先前节点和下一个节点，你可以删除或插入指针，这只有O(1)的开销。
    但正因为内存不连续，你不能计算地址来取得先前节点和后面的节点，所以你不能随机访问。而且每一个节点需要存储先前与之后的节点，它使用更多空间。
    一个图拥有两种常见的储存方式。一个邻接表。一个邻接矩阵。一个邻接矩阵可以更快速检查链接，而且你可以使用矩阵结构去解决一些问题。但是如果图是稀疏的，
    它浪费了许多空间。一个邻接表可以节约空间，但是许多操作会比矩阵更加缓慢。
 

    AI-Verson:
    只有两种方式去存储数据结构：数组（连续存储）与链表（链式存储）。如何去理解这个？难道没有哈希表、栈、队列、堆、树、图和许多其他数据结构了吗？
    当我们要分析这个问题时，应该按照递归的思考方式：自顶向下，从抽象到具体。如果你首先列出那些结构，它们其实是高级的逻辑设计。
    数组和链表才是底层的物理基本结构。那些不同的数据结构，本质上只是在特定操作规则下的数组或链表，它们仅仅拥有不同的调用接口（API）。
    举例来说，队列和栈可以通过链表或数组来实现。使用数组时，你需要去控制内存的扩容与缩容；使用链表时，你没有扩容问题，但是需要更多空间来存放节点指针。
    图拥有两种常见的存储方式：邻接表和邻接矩阵。邻接矩阵（二维数组）可以更快速地检查节点间是否存在连接，而且你可以利用矩阵运算去解决一些特定问题，但如果图是稀疏的，
    它会浪费许多空间。
    邻接表（基于链表）可以节约空间，但许多查询操作会比矩阵更加缓慢。哈希表则是使用哈希函数将 Key 映射到大数组的索引中：对于哈希冲突，拉链法利用了链表的特性，实现简单，
    但需要额外的指针空间。
    线性探测法利用了数组连续寻址的特性，不需要指针空间，但在操作和维护上会稍微复杂一些。对于树（Tree）来说：如果你使用数组来存放，它就变成了“堆”，因为堆是一棵完全二叉树。
    使用数组存储时，你不需要节点指针，操作也更简单，一个经典的例子就是二叉堆；如果你使用链表来存放，它就是最常见的树形结构。
    因为普通树往往不是完全二叉树，所以不适合用数组来存储。基于基于链表的树，人们创造了许多设计，像二叉查找树、平衡树、红黑树、线段树、B树等，用以解决不同的实际问题。
    因此，世界上有许多数据结构，你甚至可以自己发明属于自己的结构。但在物理存储级别来看，它仍然仅仅只是数组或者链表。它们的优缺点如下：数组：采用紧密、连续的内存空间存储。
    你可以进行随机访问，快速按照索引定位元素，且没有指针开销，能够节约空间。但正因为必须连续，内存申请必须一次性完成。
    如果你需要扩大空间，必须申请另一块更大的连续内存并复制所有数据，开销是 $O(N)$；如果在数组中间进行插入或删除，必须移动之后的所有元素以保持连续性，开销也是 O(N)。
    链表：不连续存储元素。每一个节点使用指针连接下一个节点，所以它没有内存扩容问题。如果你知道前驱节点和后继节点，只需修改指针即可完成插入或删除，这只有 O(1) 的开销。
    但正因为内存不连续，你不能通过计算地址来直接定位元素，所以无法进行随机访问；此外，每一个节点都需要额外存储指针，使用空间更多。

```

### Back-translate (Spoken-English)

```
    Self-Verson:
    There are only two ways to store the data structures: arrays(stored in order) and linked lists(stored by links).
    How can we understand this? Aren't these hash tables, stacks, queues, heaps, trees, graphs and many other data structures?
    When we analyze the problem, we should follow a thought that is recursive: Top-Down, from abstract to concrete.
    If you list those structures first, those are 
    heig-level structures. Arrays and linked lists are basic structures. Those structures are different arrays or linked lists with special operations. 
    They just own different APIs.
    For example, queues and stacks can be implemented by any linked lists or arrays. If with arrays, you need to handle growing space and shrinking space. 
    If with linked lists, you don't have this problem, but need more space to save the pointers.
    A graph has two common storage ways. The first is an adjacency list. The second is an adjacency matrix. 
    An adjacency matrix can improve to check link faster than an adjacency list, and you can use matrix to solve many questions. 
    But if a graph is sparse, it wastes a lot of memories. An adjacency list can save memories, but many operations will be slower.
    A hash table uses hash function to map keys in large array. To hash collisions, decoupled chain structure needs link features. 
    It is simple but needs additional space to save pointers.
    Linear probing way needs array with continues address. Here is no need of pointers, but in operations will be more complex.
    For trees: If you use array to stroe a tree, it becomes a heap, because of a heap is a complete binary tree. Using an array, 
    you don't need to store other pointers and operations will be simpler. A classic example is the binary heap. If with linked lists, 
    it's ordinary tree. So it isn't a complete binary tree, it is not suitable to use an array. Basing on link trees, 
    it likes binary search tree, AVL tree, red-black tree, segment tree, B-tree or other tree, so for different problems are not same.
    So there are many structures, even you can invent a new structure. In stored level, it is only arrays or linked lists.
    Their advantages and disadvantages are:
    Arrays can be stored in compact, contiguous memory space. You can random access and quickly by index, and it also saves space. 
    But with contiguous memory space, the memory must be allocated on one piece. So if you want to grow the array, 
    you must allocate another bigger contiguous memory space and copy all elements to new space which is O(N).
    On the other hand, if you insert or delete an element in middle, you also need to move all  behind elements which is O(N). 
    linked lists don't store contiguous elements. Every node points to the next node, so they don't have this problem. 
    If you know previous node and next node, you can insert or delete node which is 
    O(1). Because memories is not contiguous, you can't calculate previous node and next node address, and random accessing is also not allowwed. 
    Every node only need to save previous node and next node that helps taking more space.

    AI-Verson:
    There are only two ways to store data structures: arrays (stored in order) and linked lists (stored by links).How can we understand this? 
    Aren't there hash tables, stacks, queues, heaps, trees, graphs, and many other data structures?
    When we analyze this problem, we should follow a thought process that is recursive: top-down, from abstract to concrete. 
    If you list those structures first, those are high-level designs. Arrays and linked lists are the basic building blocks. 
    Those different data structures are just arrays or linked lists with special operations and different API interfaces.
    For example, queues and stacks can be implemented by either linked lists or arrays. With arrays, you need to handle growing and shrinking space. 
    With linked lists, you don't have this problem, but you need more space to save node pointers.
    A graph has two common storage ways: an adjacency list and an adjacency matrix. An adjacency matrix can check connections faster than an adjacency list, 
    and you can use matrix operations to solve many problems. But if a graph is sparse, it wastes a lot of memory. An adjacency list saves memory, 
    but many operations will be slower.A hash table uses a hash function to map keys to indices in a large array. 
    For hash collisions:Separate chaining needs linked list features. It is simple, but requires additional space to save pointers.
    Linear probing needs an array with continuous addressing. There is no need for pointers, but the operations are slightly more complex.
    For trees:If you use an array to store a tree, it becomes a heap, because a heap is a complete binary tree. Using an array, 
    you don't need to store node pointers, and operations are simpler—a classic example is the binary heap.If you use linked lists, 
    it forms an ordinary tree. Since general trees may not be complete binary trees, they are not suitable for array storage. 
    Based on linked-list trees, people created many designs like binary search trees, AVL trees, red-black trees, segment trees, 
    and B-trees for different problems.So there are many data structures, and you can even invent your own. But at the storage level, 
    it is still only arrays or linked lists.Their advantages and disadvantages are:Array: Stores data in a compact, contiguous memory space. 
    You can perform random access quickly by index, and it saves overhead space. But because memory must be contiguous, 
    allocation must be in one piece. If you want to grow the array, you must allocate another larger contiguous memory space and copy all elements, 
    which is $O(N)$. On the other hand, if you insert or delete an element in the middle, you also need to move all behind elements, 
    which is $O(N)$.Linked List: Does not store elements contiguously. Every node points to the next node, so they don't have the memory growth problem. 
    If you know the previous node and next node, you can insert or delete a node in $O(1)$ time. Because memory is not contiguous, 
    you cannot calculate addresses for random access. Additionally, every node needs to save pointers, which takes more space.
```

---

## 3. Review

### Sentence Patterns

| Pattern | Example from Pattern | Note |

Pattern
```
    1.There are only [X] ways to [action]: [Option A] and [Option B].
    2.Those [high-level concepts] are simply [Concept A/B] with special operations.
    3.At the [X] level, it is still only [A] or [B].
    4.When we analyze [problem], we should follow a thought process that is [adjective]: [Path A] to [Path B].
    5.With [Option A], you need to [handle problem]. With [Option B], you don't have this problem, but [new issue].
    6.If you use [A] to store [B], it becomes [C], because [reason].
    6.Since [Reason/Condition], it is not suitable to [Action].
```

Example from Pattern
```
    1.There are only two ways to handle concurrency: multi-threading and asynchronous I/O.
    2.Other application-layer protocols are simply specialized wrappers over them.
    3.At the hardware level, all operations are reduced to 0s and 1s.
    4.When we design system architecture, we should follow a thought process that is modular: high-level systems down to individual components.
    5.With REST APIs, you need to handle over-fetching. With GraphQL, you don't have this problem, but schema maintenance becomes complex.
    6.If you use a FIFO strategy to manage tasks, it becomes a queue, because order is preserved strictly by arrival time.
    7.Since real-time networks tolerate frame loss, TCP is not suitable for streaming audio.
```

Note
```
    Recursive: Self to self invoke until condition.
    Abstract: Don't exist in reality.
    Concrete: Exist in reality.
    Common: Usually.
    Additional: Others.
    Store data in a compact: Less space in storing memory.
```

---

### Vocabulary

| Word / Phrase | Meaning | Collocation | Example | Note |

```
    Compact:紧凑
    Additional:额外的
    Concrete:具体的
    Recursive:递归
    Adjacency:邻接
```

---