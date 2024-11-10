#### 实验总结
文件系统章节是我花时间最多的一个章节，时间主要花在了对文件系统的理解上，看源码也费了些时间。将细节通过在线文档整理如下图所示：
![ch6 基础知识](./ch6_基础知识.png)

#### 问答作业
Root Inode 的作用：
文件系统的入口点：在类 Unix 文件系统中，root inode 是文件系统层次结构的根，即 / 目录。它是访问文件系统其余部分的起始点。
存储目录信息：root inode 存储了根目录下的文件和子目录的元数据，例如它们的名称、inode 编号、文件类型（文件或目录）等。
维护文件系统结构：root inode 作为文件系统结构的起点，确保了整个文件系统的组织性和可访问性。
权限控制：root inode 还包含了访问权限信息，用于控制对根目录及其下内容的访问。
如果 Root Inode 损坏：
如果 root inode 中的内容损坏，可能会发生以下情况：

无法访问文件系统：由于 root inode 是访问文件系统的入口，如果它损坏，可能会导致整个文件系统无法挂载，用户无法访问任何文件或目录。
数据丢失：虽然文件数据可能仍然存储在磁盘上，但如果 root inode 损坏，系统可能无法定位这些数据，导致数据看似丢失。
文件系统损坏：文件系统的元数据完整性对于文件系统的健康至关重要。root inode 损坏可能导致文件系统元数据不一致，进而导致整个文件系统损坏。
恢复困难：恢复损坏的 root inode 可能非常困难，可能需要专业的数据恢复工具和专业知识。


#### 荣誉准则

1. 在完成本次实验的过程（含此前学习的过程）中，我曾分别与 以下各位 就（与本次实验相关的）以下方面做过交流，还在代码中对应的位置以注释形式记录了具体的交流对象及内容：
   无

2. 此外，我也参考了 以下资料 ，还在代码中对应的位置以注释形式记录了具体的参考来源及内容：

   我的参考资料：rCore-Tutorial-Book-v3

3. 我独立完成了本次实验除以上方面之外的所有工作，包括代码与文档。 我清楚地知道，从以上方面获得的信息在一定程度上降低了实验难度，可能会影响起评分。

4. 我从未使用过他人的代码，不管是原封不动地复制，还是经过了某些等价转换。 我未曾也不会向他人（含此后各届同学）复制或公开我的实验代码，我有义务妥善保管好它们。 我提交至本实验的评测系统的代码，均无意于破坏或妨碍任何计算机系统的正常运转。 我清楚地知道，以上情况均为本课程纪律所禁止，若违反，对应的实验成绩将按“-100”分计。