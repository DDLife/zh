# behaviour tree

- require "behaviourtree"

BT (Behavior Tree) 是 FSM (Finite State Machine)的强约束模式, 有更好的封装性和模块性 [^ten bt] . 这使得 BT 容易组合出高级的概念 [^youtube bt]

外界发送给 bt 的信号为 tick [^youtube bt intro] [^cpp bt] , 相当于游戏帧

当某个 action 处于 running, 则 tick 来临时, 会抵达 running 的 leaf node 继续执行, 直到变成 success 或 failed

## BehaviourNodeStatus

<docs-expose>

DS 对 node 设置了四种 status:

- @SUCCESS
- @FAILED
- @READY
- @RUNNING

</docs-expose>

## Visit

<docs-expose>

对 tick 进行转发和响应, 向前传播

</docs-expose>

## References

1. [行为树及其实现 · Domi●Cat](https://domicat.me/2017/03/24/behavior-tree-1/)
2. [-ten bt] [行为树的基本概念及进阶 – behaviac](https://www.behaviac.com/language/zh/concepts/)
3. [Behavior Tree | AI 分享站 - Part 3](http://www.aisharing.com/archives/tag/behavior-tree/page/3)
4. [第五期 思想 - 让生物拥有智慧 - 知乎](https://zhuanlan.zhihu.com/p/460999291)
5. [-cpp bt] [Introduction to BTs | BehaviorTree.CPP](https://www.behaviortree.dev/docs/learn-the-basics/BT_basics)
6. [Behavior Tree Quick Start Guide | Unreal Engine 4.27 Documentation](https://docs.unrealengine.com/4.27/en-US/InteractiveExperiences/ArtificialIntelligence/BehaviorTrees/BehaviorTreeQuickStart/)
7. [-youtube bt intro] [Introduction to behavior trees - Robohub](https://robohub.org/introduction-to-behavior-trees/)
8. [5 minute Behavior Tree tutorial - YouTube](https://www.youtube.com/watch?v=KeShMInMjro&list=PLFQdM4LOGDr_2KvaaS_6-0dLPWfsoSWoW&index=1) 非常推荐
9. [-youtube bt] [What is a Behavior Tree and How do they work? (BT intro part 1) - YouTube](https://www.youtube.com/watch?v=DCZJUvTQV5Q)
10. Book: [Behavior Trees in Robotics and AI](https://arxiv.org/pdf/1709.00084.pdf)
11. [BehaviourTree: 从饥荒的 Lua 脚本中抽离出的 Lua 行为树。将行为树修改为不依赖于他原本的 Class 文件，转而依赖于 Cocos2dx-lua 中的 functions 文件](https://gitee.com/anxin1225/BehaviourTree)
12. [Behavior tree (artificial intelligence, robotics and control) - Wikipedia](https://en.wikipedia.org/wiki/Behavior_tree_%28artificial_intelligence,_robotics_and_control%29)
13. [Behavior tree - Wikipedia](https://en.wikipedia.org/wiki/Behavior_tree)
