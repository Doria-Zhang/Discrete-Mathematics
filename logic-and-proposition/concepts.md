## 命题与复合命题

### 命题

**命题**（或**陈述**）是一个说明性语句，它只能是真或假，不可能两者同时成立。

## 复合命题

**复合命题** 由*子命题*及它们之间的各种联系组成的命题称为复合命题。

**原子命题** 不能被分解为更简单的命题（非复合命题）称为原子命题

## 基本逻辑运算

**合取联结**

任何两个命题可以用术语“与”联合而成一个复合命题，叫做这两个原始命题的合取联结。记作：

$$
p \land q
$$

读作“p与q”，表示p与q的合取联结。

**定义4.1** 如果$p$与$q$均为真，则 $p \land q$ 为真；否则 $p \land q$为假。

**析取联结**

任何两个命题可以用术语“或”联合而成一个复合命题，叫做这两个原始命题的析取联结。记作：

$$
p \lor q
$$

读作“p 或 q”，表示p 与 q的析取联结。

**定义4.2** 如果p与q均为假，则 $p \lor q$ 为假；否则$p \lor q$为真。

### 否定联结, $\lnot p$

给定任一命题p，都可以通过在p前面添加“不是”或“假”或在p前面插入“非”，得到另一个命题，称为p的否定联结，记作：

$$
\lnot p
$$

读作“非p”，表示p的否定联结。

**定义4.3** 如果p为真，则 $\lnot p$ 为假；如果p为假，则 $\lnot p$ 为真。

## 命题与真值表

**命题表达式**

设 $P(p, q, ...)$为一个由取值为真(T)或假(F)的逻辑变量p, q, ... 以及逻辑联结 $\land, \lor, \lnot$ 构成的表达式。
这样的表达式$P(p, q, ...)$称为一个命题。

**逻辑联结的规定优先级** 规定：
$$
\lnot 优先于 \land 优先于 \lor
$$

### 构造真值表的另一种方法

## 永真命题与永假命题

**永真命题(tautology)** 对于变量的任意值，都为真的命题。

**永假命题(contradiction)** 对于变量的任意做，都为假的命题。

既不是永真式又不是矛盾式的复合命题称为可能式(contingency). 

**定理4.1（代入原理）** 若$P(p, q, ...)$是永真命题，
则对任意命题$P_1, P_2, ...,$ 命题$P(P_1, P_2, ...)$仍然是永真命题。

## 逻辑等价

两个命题$P(p, q, ...)$ 与 $Q(p, q, ...)$如果具有*相同的真值表*，则称为*逻辑等价*的，或简称为*等价*或*相等*，记作：

$$
P(p, q, ...) \equiv Q(p, q, ..)
$$

例如：
$$
\lnot (p \land q) \equiv \lnot p \land \lnot q
$$

## 命题代数

**定理4.2** 命题满足如下定律：

    1. 幂等律
$$
  p \lor p \equiv p
$$
$$
  p \land p \equiv p
$$

    2. 结合律
$$
(p \lor q) \lor r \equiv p \lor (q \lor r)
$$
$$
  (p \land q) \and r \equiv p \land (q \land r)
$$

    3. 交换律
$$
  p \lor q \equiv q \lor p
$$
$$
  p \land q \equiv q \land p
$$

    4. 分配律
$$
  p \lor (q \land r) \equiv (p \lor q) \and (p \lor r)
$$
$$
  p \land (q \lor r) \equiv (p \land q) \lor (p \land r)
$$

    5. 同一律
$$
  p \land T \equiv p, p \lor F \equiv p
$$
$$
p \lor T \equiv T, p \land F \equiv F
$$

    6. 互补律
$$
  p \lor \lnot p \equiv T, p \land \lnot p \equiv F
$$
$$
  \lnot T \equiv F, \lnot F \equiv T
$$

    7. 对合律
$$
  \lnot \lnot p \equiv p
$$

    8. DeMorgan律
$$
\lnot(p \lor q) \equiv \lnot p \land \lnot q
$$
$$
\lnot(p \land q) \equiv \lnot p \lor \lnot q
$$

```javascript
9.吸收律
```

$$
\begin{array}{l}{p \vee(p \wedge q) \equiv p} \\ {p \wedge(p \vee q) \equiv p}\end{array}
$$

```
10.否定律
```

$$
\begin{array}{l}{p \vee \neg p \equiv \mathbf{T}} \\ {p \wedge \neg p \equiv \mathbf{F}}\end{array}
$$



## 条件语句与双条件语句

**条件语句** 具有形式“如果p则q”的语句称为条件语句。记作：
$$
p \implies q
$$

常读作“p蕴含q”或者“仅当q时有p”。
$$
\begin{array}{l}{p \rightarrow q \equiv \neg p \vee q} \\ {p \rightarrow q \equiv \neg q \rightarrow \neg p} \\ {p \vee q \equiv \neg p \rightarrow q} \\ {p \wedge q \equiv \neg(p \rightarrow \neg q)}\end{array}
$$

$$
\begin{array}{l}{\neg(p \rightarrow q) \equiv p \wedge \neg q} \\ {(p \rightarrow q) \wedge(p \rightarrow r) \equiv p \rightarrow(q \wedge r)} \\ {(p \rightarrow r) \wedge(q \rightarrow r) \equiv(p \vee q) \rightarrow r} \\ {(p \rightarrow q) \vee(p \rightarrow r) \equiv p \rightarrow(q \vee r)} \\ {(p \rightarrow r) \vee(q \rightarrow r) \equiv(p \wedge q) \rightarrow r}\end{array}
$$

**真值表**

| p    | q    | $p \implies q$ |
| ---- | ---- | -------------- |
| T    | T    | T              |
| T    | F    | F              |
| F    | T    | T              |
| F    | F    | T              |

（为何 $(F, F) = T$ ？）

**双条件语句** 具有形式“p当且仅当q”的语句称为双条件语句。记作：
$$
p \iff q
$$

$$
\begin{array}{l}{p\iff q \equiv(p \implies q) \wedge(q \implies p)} \\ {p \iff q \equiv \neg p \iff \neg q} \\ {p \iff q \equiv(p \wedge q) \vee(\neg p \wedge \neg q)} \\ {\neg(p \iff q) \equiv p \iff \neg q}\end{array}
$$

| p    | q    | p $\iff$ q |
| ---- | ---- | ---------- |
| T    | T    | T          |
| T    | F    | F          |
| F    | T    | F          |
| F    | F    | T          |

