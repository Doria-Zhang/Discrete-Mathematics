# Application of number theory

## 同余应用

### 伪随机数

选择4个整数: 模数 $m$、倍数 $a$、增量 $c$、种子 $x_0$，满足对于所有 $n$
$$
x_{n+1}=\left(a x_{n}+c\right) \bmod m
$$

### 校验码

## 密码学

#### RSA算法

选择两个大素数 $p$ 和 $q$, 计算
$$
n=pq
$$
取 $n$ 的欧拉函数:
$$
\phi(n)=(p-1)(q-1)
$$
随机取一个小于 $\phi(n)$ 的整数 $e$, 使得
$$
\gcd(e,\phi(n))=1
$$
计算$e$对于 $\phi(n)$ 的模逆 $d$:
$$
ed\equiv1(\bmod \phi(n))
$$
将 $(n,e)$ 作为公钥, $(n,d)$作为私钥. 为了加密一个信息 $m$:
$$
m^e\equiv c(\bmod n)
$$
即 $c$ 是加密后的信息, 然后利用私钥解密
$$
c^d\equiv m(\bmod n)
$$
下面我们证明这样的解密是成立的, 只需证
$$
m^{ed}=m(\bmod n)
$$
由于
$$
ed\equiv1(\bmod \phi(n))
$$
所以存在 $h$:
$$
ed=h \phi(n)+1
$$
即证明
$$
m^{h \phi(n)+1} \equiv m(\bmod n)
$$
在大多数情况下, $\gcd(m,n)=1$, 于是由欧拉定理
$$
m^{ \phi(n) }\equiv 1 \quad(\bmod n)
$$
该式显然成立.

如果 $m,n$ 不互质, 不妨设
$$
m=kp
$$
因为
$$
m<n \implies k<q \implies \gcd(k,q)=1
$$
所以由费马小定理
$$
(kp)^{q-1}\equiv1(\bmod q)
$$
所以
$$
\left[(\mathrm{kp})^{q-1}\right]^{h(p-1)} \times k p \equiv k p(\bmod q)
$$
即
$$
(\mathrm{kp})^{\mathrm{ed}} \equiv \mathrm{kp} \quad(\bmod \mathrm{q})
$$
这说明存在 $t$:
$$
(\mathrm{kp})^{\mathrm{ed}}=\mathrm{tq}+\mathrm{kp}
$$
$t$ 必须为 $p$ 的倍数:
$$
(k p)^{e d}=t^{\prime} p q+k p
$$
所以
$$
m^{e d} \equiv m \quad(\bmod n)
$$
