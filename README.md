# 设计模式

- ## 创建型模式

    - ### 单例模式（singleton pattern）
      
        - &emsp;&emsp;单例模式，也叫单子模式，是一种常用的软件设计模式。在应用这个模式时，单例对象的类必须保证只有一个实例存在。许多时候整个系统只需要拥有一个的全局对象，这样有利于我们协调系统整体的行为。比如在某个服务器程序中，该服务器的配置信息存放在一个文件中，这些配置数据由一个单例对象统一读取，然后服务进程中的其他对象再通过这个单例对象获取这些配置信息。这种方式简化了在复杂环境下的配置管理。
      
        - &emsp;&emsp;实现单例模式的思路是：一个类能返回对象一个引用(永远是同一个)和一个获得该实例的方法（必须是静态方法，通常使用getInstance这个名称）；当我们调用这个方法时，如果类持有的引用不为空就返回这个引用，如果类保持的引用为空就创建该类的实例并将实例的引用赋予该类保持的引用；同时我们还将该类的构造函数定义为私有方法，这样其他处的代码就无法通过调用该类的构造函数来实例化该类的对象，只有通过该类提供的静态方法来得到该类的唯一实例。
      
    - ### 简单工厂模式（simple factory pattern）
          
        - &emsp;&emsp;简单工厂模式是属于创建型模式，又叫做静态工厂方法（Static Factory Method）模式。简单工厂模式是由一个工厂对象决定创建出哪一种产品类的实例。简单工厂模式是工厂模式家族中最简单实用的模式，可以理解为是不同工厂模式的一个特殊实现。
          
    -  ### 工厂方法模式 (factory method pattern)

        - &emsp;&emsp;工厂方法设计模式

    - ### 抽象工厂模式 (abstract factory pattern)

        - &emsp;&emsp;抽象工厂模式

    - ### 创建者模式 (builder pattern)

        - &emsp;&emsp;创建者模式


- ## 行为模式

    - ### 命令模式（command pattern）

        - &emsp;&emsp;将请求封装成对象，以便使用不同的请求、队列或者日志来参数化其他对象。命令模式也支持可撤销的操作。从而实现“行为请求者”与“行为实现者”的松耦合。

        - #### 命令模式成员
            
            - 抽象命令(Command)：定义命令的接口，声明执行的方法（execute、undo）
            - 具体命令(ConcreteCommand)：命令接口实现对象，通常会持有接收者，并调用接收者的功能来完成命令要执行的操作
            - 接收者(Receiver)：执行命令的对象
            - 请求者(Invoker)：调用命令对象执行请求
            
    - ### 观察者模式 (observer pattern)

        - &emsp;&emsp;观察者模式

    - ### 中介者模式

        - &emsp;&emsp;中介者模式

    - ### 状态模式 (state pattern)

        - &emsp;&emsp;状态模式

    - ### 策略模式 (strategy pattern)

        - &emsp;&emsp;策略模式


- ## 结构型模式

    - ### 桥接模式 (bridge pattern)

        - &emsp;&emsp;桥接模式的功能在于将两个原本不相关的类结合在一起，然后利用两个类中的方法和属性，输出一份新的结果。

    - ### 外观模式 (facade pattern)

        - &emsp;&emsp;外观模式（Facade Pattern）隐藏系统的复杂性，并向客户端提供了一个客户端可以访问系统的接口。这种类型的设计模式属于结构型模式，它向现有的系统添加一个接口，来隐藏系统的复杂性。

    - ### 享元模式 (flyweight pattern)

        - &emsp;&emsp;享元模式

    - ### 代理模式 (proxy pattern)

        - &emsp;&emsp;代理模式

    - ### 适配器模式 (adapter pattern)

        - &emsp;&emsp;将一个类的接口转换成客户希望的另外一个接口。Adapter 模式使得原本由于接口不兼容而不能一起工作的那些类可以一起工作。

        - #### 使用场景

            - 需要的东西在面前，但却不能用，而短时间又无法改造它，于是就想办法适配

            - 系统的数据和行为都正确，但接口不符时，应该考虑使用适配器，目的是使控制范围之外的一个原有对象与某个接口匹配。适配器模式只要应用于希望复用一些现存的类，但接口又与复用环境要求不一致的情况

            - 这是一种“亡羊补牢”的方法。

            - 首选的方法应该是重构代码，统一接口。

            - 用于 两个类功能相同或相似

            - 在项目中需要使用第三方组件时，常用到此模式

    - ### 装饰模式 (decorator pattern)

        - &emsp;&emsp;装饰器模式（Decorator Pattern）允许向一个现有的对象添加新的功能，同时又不改变其结构。这种类型的设计模式属于结构型模式，它是作为现有的类的一个包装。