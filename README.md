# hadoop
本项目打算做一个基于hadoop的分布式文件系统，用来存储一些常用的文件。
                                                        大数据分析与处理
1.可视化分析
大数据分析的使用者有大数据分析专家，同时还有普通用户，但是他们二者对于大数据分析最基本的要求就是可视化分析，因为可视化分析能够直观的呈现大数据特点，同时能够非常容易被读者所接受，就如同看图说话一样简单明了。
2. 数据挖掘算法
 大数据分析的理论核心就是数据挖掘算法，各种数据挖掘的算法基于不同的数据类型和格式才能更加科学的呈现出数据本身具备的特点，也正是因为这些被全世界统计 学家所公认的各种统计方法（可以称之为真理）才能深入数据内部，挖掘出公认的价值。另外一个方面也是因为有这些数据挖掘的算法才能更快速的处理大数据，如 果一个算法得花上好几年才能得出结论，那大数据的价值也就无从说起了。
3. 预测性分析
 大数据分析最终要的应用领域之一就是预测性分析，从大数据中挖掘出特点，通过科学的建立模型，之后便可以通过模型带入新的数据，从而预测未来的数据。
4. 语义引擎
 非结构化数据的多元化给数据分析带来新的挑战，我们需要一套工具系统的去分析，提炼数据。语义引擎需要设计到有足够的人工智能以足以从数据中主动地提取信息。
5.数据质量和数据管理。 大数据分析离不开数据质量和数据管理，高质量的数据和有效的数据管理，无论是在学术研究还是在商业应用领域，都能够保证分析结果的真实和有价值。
大数据分析的基础就是以上五个方面，当然更加深入大数据分析的话，还有很多很多更加有特点的、更加深入的、更加专业的大数据分析方法。
 
大数据的技术
数据采集： ETL工具负责将分布的、异构数据源中的数据如关系数据、平面数据文件等抽取到临时中间层后进行清洗、转换、集成，最后加载到数据仓库或数据集市中，成为联机分析处理、数据挖掘的基础。
数据存取： 关系数据库、NOSQL、SQL等。
基础架构： 云存储、分布式文件存储等。
数据处理： 自然语言处理(NLP，Natural Language Processing)是研究人与计算机交互的语言问题的一门学科。处理自然语言的关键是要让计算机”理解”自然语言，所以自然语言处理又叫做自然语言理解也称为计算语言学。一方面它是语言信息处理的一个分支，另一方面它是人工智能的核心课题之一。
统计分析：  假设检验、显著性检验、差异分析、相关分析、T检验、 方差分析 、 卡方分析、偏相关分析、距离分析、回归分析、简单回归分析、多元回归分析、逐步回归、回归预测与残差分析、岭回归、logistic回归分析、曲线估计、 因子分析、聚类分析、主成分分析、因子分析、快速聚类法与聚类法、判别分析、对应分析、多元对应分析（最优尺度分析）、bootstrap技术等等。
数据挖掘： 分类 （Classification）、估计（Estimation）、预测（Prediction）、相关性分组或关联规则（Affinity grouping or association rules）、聚类（Clustering）、描述和可视化、Description and Visualization）、复杂数据类型挖掘(Text, Web ,图形图像，视频，音频等)
模型预测 ：预测模型、机器学习、建模仿真。
结果呈现： 云计算、标签云、关系图等。
 
大数据的处理
1. 大数据处理之一：采集
大数据的采集是指利用多个数据库来接收发自客户端（Web、App或者传感器形式等）的 数据，并且用户可以通过这些数据库来进行简单的查询和处理工作。比如，电商会使用传统的关系型数据库MySQL和Oracle等来存储每一笔事务数据，除 此之外，Redis和MongoDB这样的NoSQL数据库也常用于数据的采集。
在大数据的采集过程中，其主要特点和挑战是并发数高，因为同时有可能会有成千上万的用户 来进行访问和操作，比如火车票售票网站和淘宝，它们并发的访问量在峰值时达到上百万，所以需要在采集端部署大量数据库才能支撑。并且如何在这些数据库之间 进行负载均衡和分片的确是需要深入的思考和设计。
2. 大数据处理之二：导入/预处理
虽然采集端本身会有很多数据库，但是如果要对这些海量数据进行有效的分析，还是应该将这 些来自前端的数据导入到一个集中的大型分布式数据库，或者分布式存储集群，并且可以在导入基础上做一些简单的清洗和预处理工作。也有一些用户会在导入时使 用来自Twitter的Storm来对数据进行流式计算，来满足部分业务的实时计算需求。
导入与预处理过程的特点和挑战主要是导入的数据量大，每秒钟的导入量经常会达到百兆，甚至千兆级别。
3. 大数据处理之三：统计/分析
统计与分析主要利用分布式数据库，或者分布式计算集群来对存储于其内的海量数据进行普通 的分析和分类汇总等，以满足大多数常见的分析需求，在这方面，一些实时性需求会用到EMC的GreenPlum、Oracle的Exadata，以及基于 MySQL的列式存储Infobright等，而一些批处理，或者基于半结构化数据的需求可以使用Hadoop。
统计与分析这部分的主要特点和挑战是分析涉及的数据量大，其对系统资源，特别是I/O会有极大的占用。
4. 大数据处理之四：挖掘
与前面统计和分析过程不同的是，数据挖掘一般没有什么预先设定好的主题，主要是在现有数 据上面进行基于各种算法的计算，从而起到预测（Predict）的效果，从而实现一些高级别数据分析的需求。比较典型算法有用于聚类的Kmeans、用于 统计学习的SVM和用于分类的NaiveBayes，主要使用的工具有Hadoop的Mahout等。该过程的特点和挑战主要是用于挖掘的算法很复杂，并 且计算涉及的数据量和计算量都很大，常用数据挖掘算法都以单线程为主。
 
整个大数据处理的普遍流程至少应该满足这四个方面的步骤，才能算得上是一个比较完整的大数据处理。
