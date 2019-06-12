# 使用Typora Markdown画图

## 时序图(Sequence)
Typora时序图是依托于[js-sequence](https://bramp.github.io/js-sequence-diagrams/)实现。来看一个例子：

~~~gfm
 ```sequence
 Alice->Bob: Hello Bob, how are you?
 Note right of Bob: Bob thinks
 Bob-->Alice: I am good thanks!
 ```
~~~

![Sequence](http://support.typora.io/media/diagrams/Snip20160816_1.png)

其他网上例子，你可以copy下去试下：
~~~gfm
 ```sequence
Title: 标题：复杂使用
对象A->对象B: 对象B你好吗?（请求）
Note right of 对象B: 对象B的描述
Note left of 对象A: 对象A的描述(提示)
对象B-->对象A: 我很好(响应)
对象B->小三: 你好吗
小三-->>对象A: 对象B找我了
对象A->对象B: 你真的好吗？
Note over 小三,对象B: 我们是朋友
participant C
Note right of C: 没人陪我玩
 ```
~~~


## 流程图(Flowchart)
Typora流程图依托于[flowchart.js](http://flowchart.js.org/)实现。来看个例子：

~~~gfm
 ```flow
st=>start: Start
op=>operation: Your Operation
cond=>condition: Yes or No?
e=>end

st->op->cond
cond(yes)->e
cond(no)->op
 ```
~~~

![Flowchart](http://support.typora.io/media/diagrams/Snip20160816_2.png)

其他网上例子，你可以copy下去试下：
~~~gfm
 ```flow
st=>start: 开始框
op=>operation: 处理框
cond=>condition: 判断框(是或否?)
sub1=>subroutine: 子流程
io=>inputoutput: 输入输出框
e=>end: 结束框
st->op->cond
cond(yes)->io->e
cond(no)->sub1(right)->op
 ```
~~~


## mermaid diagrams
Typora另外还结合[Mermaid](https://mermaidjs.github.io/)，支持了Mermaid模式下的时序图(sequence)，流程图(flowchart)和甘特图(Gantt)。

### 时序图(mermaid sequence)
~~~gfm
 ```mermaid
 %% Example of sequence diagram
  sequenceDiagram
    Alice->>Bob: Hello Bob, how are you?
    alt is sick
    Bob->>Alice: Not so good :(
    else is well
    Bob->>Alice: Feeling fresh like a daisy
    end
    opt Extra response
    Bob->>Alice: Thanks for asking
    end
 ```
~~~

![mermaid sequence](http://support.typora.io/media/diagrams/Snip20160816_3.png)

其他网上例子，可以copy下去试试哦：
~~~gfm
 ```mermaid
 %% 时序图例子,-> 直线，-->虚线，->>实线箭头
  sequenceDiagram
    participant 张三
    participant 李四
    张三->王五: 王五你好吗？
    loop 健康检查
        王五->王五: 与疾病战斗
    end
    Note right of 王五: 合理 食物 <br/>看医生...
    李四-->>张三: 很好!
    王五->李四: 你怎么样?
    李四-->王五: 很好!
 ```
~~~


### 流程图(mermaid flowchart)

~~~gfm
 ```mermaid
graph LR
A[Hard edge] -->B(Round edge)
    B --> C{Decision}
    C -->|One| D(Result one)
    C -->|Two| E[Result two]
 ```
~~~

![mermaid flowchart](http://support.typora.io/media/diagrams/Snip20160816_4.png)

### 甘特图(mermaid Gantt)

~~~gfm
 ```mermaid
%% Example with selection of syntaxes
        gantt
        dateFormat  YYYY-MM-DD
        title Adding GANTT diagram functionality to mermaid

        section A section
        Completed task            :done,    des1, 2014-01-06,2014-01-08
        Active task               :active,  des2, 2014-01-09, 3d
        Future task               :         des3, after des2, 5d
        Future task2              :         des4, after des3, 5d

        section Critical tasks
        Completed task in the critical line :crit, done, 2014-01-06,24h
        Implement parser and jison          :crit, done, after des1, 2d
        Create tests for parser             :crit, active, 3d
        Future task in critical line        :crit, 5d
        Create tests for renderer           :2d
        Add to mermaid                      :1d

        section Documentation
        Describe gantt syntax               :active, a1, after des1, 3d
        Add gantt diagram to demo page      :after a1  , 20h
        Add another diagram to demo page    :doc1, after a1  , 48h

        section Last section
        Describe gantt syntax               :after doc1, 3d
        Add gantt diagram to demo page      : 20h
        Add another diagram to demo page    : 48h
 ```
~~~

![mermaid Gantt](http://support.typora.io/media/diagrams/Snip20160816_5.png)



##  注意事项
* 由于目前 standard Markdown、CommonMark、GFM 暂不支持画图，所以建议使用对应工具画图，导出图片，插入到Markdown文本中，保证不丢失。




----
## 参考文献
* [Draw Diagrams With Markdown](http://support.typora.io/Draw-Diagrams-With-Markdown/) 
* [typora-wiki-github](https://github.com/typora/wiki-website)
* [Mermaid document](https://mermaidjs.github.io/)
