# 用Markdown画图

## mermaid格式

```mermaid

graph TB
subgraph one
	a1 --> a2
end
subgraph two
	b1 --- b2
end
subgraph three
	c1 -.- c2
end
c1 --"This is a text(one)"--> b2
```

```mermaid
graph LR
	id1[This is the text in the box]
	id2(This is the text in the box)
	id3>This is the text in the box]
	id4{This is the text in the box}
	id5{{This is the text in the box}}
	id6[/This is the text in the box/]
	id7[\This is the text in the box\]
	id8[/Trapezoid\]
	id9[\Trapezoid alt/]
	id4 =="This is a text (one)"==> id1 === |"This is a text (two)"|id2 === id3
	id4 --> id5 --- id6 --- id7
	id4 --This is a text--- id8 -.This is a text.- id9
```

```mermaid
pie title Animal
	"Dog"   : 114
	"Cat"   : 49
	"Panda" : 58
```

## 用flow格式
```flow
st=>start: Start
end=>end: End
in=>inputoutput: Input Score Number
out=>inputoutput: Output Student Count
condNot=>condition: n != -1
cond1=>condition: 1<=n<=59
cond2=>condition: 60<=n<=79
cond3=>condition: 80<=n<=89
else=>condition: else
op1=>operation: x1 += 1
op2=>operation: x2 += 1
op3=>operation: x3 += 1
op4=>operation: x4 += 1
op5=>end: End
st->in->condNot
condNot(no)->op5
condNot(yes)->cond1(no)->cond2(no)->cond3(no)->else(no)->end
cond1(yes)->op1
cond2(yes)->op2
cond3(yes)->op3
else(yes)->op4
op1->out
op2->out
op3->out
op4->out
out->end
```
