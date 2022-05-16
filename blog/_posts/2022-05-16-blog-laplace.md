---
layout: post
title: 라플라스 근사 (Laplace Approximation)
# description: >
#   Howdy! This is an example blog post that shows several types of HTML content supported in this theme.
sitemap: false
hide_last_modified: true
---

<br>

> 본 글은 *Peter D.Hoff*의 *A First Course in Bayesian Statistical
Methods* 와 *David J.C. MacKay*의 *Informationm Theory, Inference, and
Learning Algorithms* 을 참고하였다. 

<br> 


### Method


라플라스 근사는 연속형 변수의 조건부 분포를 정규분포로 근사하는 것이다. 그러므로 임의의 분포인 사후분포를 정규분포로 근사할 수 있다.

<br>

#### Univariate Case


$$\theta$$에 대한 일변량 분포에 대해서 생각해보자.

$$
p(\theta \lvert D )  = \frac{1}{Z} p(\theta, D) = \frac{1}{Z} p(D | \theta) p(\theta) =  \frac{1}{Z} f(\theta).
$$

여기서, $$Z$$는 정규화 상수다. 

$$ 
Z = \int p(\theta, D)\, d \theta = \int f(\theta)\,d\theta
$$

라플라스 근사는 $$p(\theta \lvert D )$$를 평균이 $$\theta_0$$이고, 분산이 $$A^{-1}$$인 정규분포로 근사하는 것이다.

$$
p(\theta | D ) \approx \mathcal{N}(\theta\,; \theta_0, A^{-1} )
$$

그러므로 $$\theta_0$$와 $$A^{-1}$$를 알아야 한다. 구하는 방법은 다음과 같다.

<br>

* 분포의 **최빈값(Mode)** 즉, $$p(\theta \lvert D )$$의 국소 최대값  $$\theta_0$$ 구해야 한다.

$$
\begin{gathered}
\dfrac{df(\theta)}{d\theta} = 0
\end{gathered}
$$

이 되는 $$\theta_0$$를 구한다. 이때, 비정규화 밀도함수, $$f(\theta)$$를 이용한다. 계산 방법으로는 직접 계산하여 정확한 해를 구하거나 뉴턴-랩슨 방법으로 수치적으로 해를 찾을 수 있다.

* $$\log f(\theta)$$의 **테일러 전개(Taylor Expansion)** 를 이용하여 정규분포 형태로 만든다.

$$
\log f(\theta) = q(\theta) = q(\theta_0) + q'(\theta_0)(\theta - \theta_0) + \frac{q''(\theta_0)}{2} (\theta - \theta_0)^{2} + \cdots. 
$$

$$\log f(\theta)$$의 테일러 전개는 위의 식과 같다. 이차항까지만 전개하여 근사한다.

$$
q(\theta) \approx q(\theta_0) + 0 - \left (- \frac{q''(\theta_0)}{2} \right) (\theta - \theta_0)^{2}.
$$

양변에 지수함수를 취하면,

$$
f(\theta) \approx f(\theta_0) \times \text{exp} \left \{-\frac{1}{2} A\, (\theta - \theta_0)^{2}  \right \}.
$$

이 된다. 여기서 A는 $$A = - q''(\theta_0) = -\frac{d^2}{d\theta^2} \log f(\theta)\Bigr\lvert_{\theta = \theta_0}$$ 이다. 또한,  $$p(\theta \lvert D)$$의 정규화 상수 $$Z$$를 다음과 같은 정규화 상수 $$Z_Q$$로 근사시킬 수 있다. 

$$
Z_Q = \sqrt{\dfrac{2\pi}{A}}f(\theta_0).
$$

그러므로 $$p(\theta \lvert D)$$는 정규분포로 근사가 가능하게 된다.

$$
p(\theta | D) \approx \mathcal{N}(\theta_0, A^{-1}) =  \dfrac{1}{\sqrt{2\pi A^{-1}}} \text{exp}\left\{- \dfrac{(\theta - \theta_0)^2}{2A^{-1}} \right\}
$$


<br>

#### Multivariate Case



다변량 분포도 일변량과 동일하게 적용하면 된다. 모수 $$\boldsymbol{\theta}$$가 $$K$$차원에 있다고 하자.$$(\boldsymbol{\theta} \in \mathbb{R}^{K})\,\,$$ 그리고 $$\boldsymbol{\theta}$$에 대한 사후분포는 $$p(\boldsymbol{\theta} \lvert D) = (1/Z)e^{\,\log f(\boldsymbol{\theta})}$$이다.


지수 부분의 $$\log f(\boldsymbol{\theta})$$를 근사하면 다음과 같다.

$$
\begin{gathered}
\log f(\boldsymbol{\theta}) \approx \log f(\boldsymbol{\theta_0}) + (\boldsymbol{\theta} - \boldsymbol{\theta_0})^{T}\mathbf{g} - \frac{1}{2} (\boldsymbol{\theta} - \boldsymbol{\theta_0})^{T} \mathbf{A}\, (\boldsymbol{\theta} - \boldsymbol{\theta_0}), \\
\mathbf{g} := \nabla \log f(\boldsymbol{\theta}) \Bigr|_{\boldsymbol{\theta} = \boldsymbol{\theta_0}}\,\,, \quad \mathbf{A} := - \nabla\nabla \log f(\boldsymbol{\theta}) \Bigr|_{\boldsymbol{\theta} = \boldsymbol{\theta_0}} = - \dfrac{\partial^2}{\partial\boldsymbol{\theta} \partial\boldsymbol{\theta}^T} \log f(\boldsymbol{\theta}) \Bigr|_{\boldsymbol{\theta} = \boldsymbol{\theta_0}}
\end{gathered}
$$

여기서, $$\boldsymbol{\theta_0}$$는 함수 $$f(\boldsymbol{\theta})$$의 최빈값(mode)이다. 또한, $$\boldsymbol{\theta_0}$$가 최빈값이므로 $$\boldsymbol{\theta_0}$$에서 gradient 부분$$(\mathbf{g})$$은 0이 되어 사라진다. 일변량일 때와 마찬가지로 양변에 지수를 취하면 다음과 같은 식이 된다.

$$
p(\boldsymbol{\theta} \lvert D) = \dfrac{1}{Z} f(\boldsymbol{\theta}) \approx  \dfrac{1}{Z}f(\boldsymbol{\theta_0}) \times\text{exp} \left\{- \frac{1}{2} (\boldsymbol{\theta} - \boldsymbol{\theta_0})^{T} \mathbf{A}\, (\boldsymbol{\theta} - \boldsymbol{\theta_0}) \right \}
$$

$$p(\boldsymbol{\theta} \lvert D)$$의 정규화 상수 $$Z$$를 다음과 같은 정규화 상수로 근사시킬 수 있다. 

$$
Z  \approx f(\boldsymbol{\theta_0}) \sqrt{\dfrac{(2\pi)^K}{|\mathbf{A}|} }
$$

그래서 사후분포 $$p(\theta \lvert D)$$를 $$K$$차원의 다변량 정규분포로 근사가 가능하다.

$$
p(\boldsymbol{\theta} \lvert D) \approx \mathcal{N}_{K}(\boldsymbol{\theta_0}, \mathbf{A}^{-1})
$$


<br>


### Example


#### The Binomial Model


* 사전분포(prior): $$\theta \sim \text{Beta}(1,1)$$.
* 자료(Data): $$y_i \stackrel{iid}{\sim} \text{Bernoulli}(\theta)$$, $$i=1,2,\ldots, 129$$. 
* 사후분포(posterior): $$\theta \, \lvert \, y_1,\ldots,y_{129} \sim  Beta(119,12) \, (\because \sum_i^{129}y_i = 118)$$


<br>

$p(\theta \lvert D)$의 비정규화 밀도함수 $f(\theta)$와 밀도함수의 1차 미분한  $f'(\theta)$에 대한 분포 형태는 다음과 같다.

``` r
f=function(x,a=1,b=1){
 (x^(a+118-1))*((1-x)^(b+11-1))
}

df=function(x,a=1,b=1){
    (x^(a+118-2))*((1-x)^(b+11-2))*((a+118-1)*(1-x)-(b+11-1)*x)
}
```

<img src="https://swpark0413.github.io/assets/img/blog/Laplace_files/figure-gfm/density-1.png" style="display: block; margin: auto;" />

두 그림을 통해서 밀도함수의 최빈값은 대략 0.9 근처에 있는 것을 알 수
있다. 최빈값을 구하기 위해서는 직접 계산하는 방법 또는 뉴턴-랩슨 방법을
이용하여 수치적으로 구할 수 있다. 뉴턴-랩슨 함수는 다음과 같다.

``` r
NRM= function(init, f,epsilon){
  library(numDeriv)
    x=init
    fx=f(x)
    fpx=genD(func = f, x = x)$D[1]
    proc=xf=x-(fx/fpx)
    diff=xf-init
    iter=1
    while(abs(diff)>epsilon ){
      x=xf
      fx=f(x)
      fpx=genD(func = f, x = x)$D[1]
      xf=x-(fx/fpx)
      proc=c(proc,xf)
      diff=proc[iter+1]-proc[iter]
      iter=1+iter
    }
    return(list(root=xf,iteration=iter,Xs=proc))
}
```

``` r
result=NRM(0.9,df,1e-32)
NRM(0.9,df,1e-32)
```

    ## $root
    ## [1] 0.9147287
    ## 
    ## $iteration
    ## [1] 7
    ## 
    ## $Xs
    ## [1] 0.9263889 0.9132672 0.9147566 0.9147287 0.9147287 0.9147287 0.9147287

``` r
mu=result$root
mu
```

    ## [1] 0.9147287

``` r
(119-1)/(119+12-2) # Mode of Beta distribution
```

    ## [1] 0.9147287

베타 분포$$(Beta(a,b))$$의 최빈값(mode)은 $$\frac{a-1}{a+b-2}$$ for $$a,b >1$$이다. 뉴턴-랩슨 방법을 이용한 것과 직접 계산한 값과 동일하다는 것을 알 수 있다.

<br>

정규분포의 분산을 구하기 위해 $$A$$를 계산해보면,

$$
\begin{aligned}
A & = - \frac{d^2}{d\theta^2} \log f(\theta)\Bigr|_{\theta = \theta_0} \\
& = - \frac{d^2}{d\theta^2} \left(\log  (\theta^{1+\sum_{i}^{129}y_i -1}) - \log(1-\theta)^{1+129-\sum_{i}^{129}y_i -1}\right)\\ 
 & = \left[\dfrac{1+\sum_{i}^{129}y_i -1}{\theta^2} + \dfrac{1+129-\sum_{i}^{129}y_i -1}{(1-\theta)^2} \right ]_{\theta = \theta_0}
\end{aligned}
$$

이 된다.

``` r
sigma=(((1+118-1)/mu^2) + (1+129-118-1)/((1-mu)^2))^(-1)
sigma
```

    ## [1] 0.0006046521

<br>

그래프를 그려보면 사후분포 $$Beta(119,12)$$와 라플라스 근사를 이용하여
도출된 정규분포 $$\mathcal{N}(0.9147287,
6.0465209^{-4})$$ 형태는 매우 비슷한 것을 알 수 있다.

``` r
x = seq(0,1,by=0.001)
plot(x,dnorm(x,mu,sqrt(sigma)),col="red",type="l",lwd=2, lty=2,
     main="Laplace method",
     xlab=expression(theta),ylab="",xlim=c(0.8,1.0))
sc=integrate(f,0,1)
lines(x,f(x)/(sc$value), lty=1, lwd=2, col="blue")
abline(v=mu,lty=3,lwd=2)
legend("topleft",c("Posterior","Approximation"),col=c("blue","red"),lwd=c(2,2),lty=c(1,2))
```

<img src="https://swpark0413.github.io/assets/img/blog/Laplace_files/figure-gfm/laplace-1.png" style="display: block; margin: auto;" />
