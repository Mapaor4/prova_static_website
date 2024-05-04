# Funció gamma i integrals Gaussianes

## Funció gamma

### Definició

*Per valors reals positius $(z>0)$ es defineix:*

$$
\boxed{\Gamma(z)\equiv\int_0^\infty x^{z-1}e^{-x}dx}
$$

### Propietats

$$
\boxed{\Gamma(z+1)=z\cdot\Gamma(z)}
$$

$$
\boxed{\Gamma(n+1)=n!}
$$

$$
\Gamma(z)\Gamma(1-z)=\frac{\pi}{\sin (\pi z)}
$$

### Definició per valors negatius

*Per valors reals negatius, s’utilitzen les propietats.*

$$
\Gamma(z)=\frac{\Gamma(z+1)}{z}
$$

$$
\Gamma(z)=\frac{\pi}{\sin (\pi z)}\frac{1}{\Gamma(1-z)}
$$

- *Exemple: Càlcul del valor de $\Gamma(-1/2)$*
    
    $$
    \Gamma(-1/2)=\frac{1}{-1/2}\Gamma(1/2)=-2\sqrt{\pi}
    $$
    
    $$
    \Gamma(-1/2)=\frac{\pi}{\sin(-\pi/2)}\frac{1}{\Gamma(1+1/2)}=\frac{\pi}{-1}\frac{2}{\sqrt\pi}=-2\sqrt{\pi}
    $$
    

### Alguns valors concrets

$$
\begin{aligned}
\hspace{-1.2em}\Gamma(0)&=\nexists
\end{aligned}

\\[0.5em]
\hspace{-1.2em}\boxed{\Gamma(1/2)=\sqrt{\pi}}
\\[0.9em]

\begin{aligned}
\Gamma(1)&=0!=1
\\[0.5em]
\Gamma(3/2)&=\frac{\sqrt{\pi}}{2}
\\[0.9em]
\Gamma(2)&=1
\\[0.5em]
\Gamma(5/2)&=\frac{3\sqrt{\pi}}{4}
\\[0.5em]
\Gamma(7/2)&=\frac{15\sqrt{\pi}}{8}
\\[2.5em]

\Gamma(-1/2)&=-2\sqrt{\pi}
\\[0.5em]
\Gamma(-3/2)&=\frac{4}{3}\sqrt{\pi}
\\[0.5em]
\Gamma(-5/2)&=-\frac{8}{15}\sqrt{\pi}
\\[0.9em]
\Gamma(-n)&=\nexists
\end{aligned}
$$

### Càlcul de $\Gamma(\frac{1}{2})=\sqrt{\pi}$

*Solució integral Gaussiana:* *[Vídeo demo](https://www.youtube.com/watch?v=9CgOthUUdw4)*

$$
\boxed{\int_{-\infty}^\infty e^{-x^2}dx=\sqrt{\pi}}
$$

*Sabent el valor d’aquesta integral podem calcular $\Gamma(\frac{1}{2})$*

$$
\sqrt{\pi}=\int_{-\infty}^{\infty} e^{-x^2}dx=2 \int_0^{\infty} e^{-x^2}dx=2 \int_0^{\infty} \frac{e^{-t}}{2 \sqrt{t}} d t=\int_0^{\infty} t^{-\frac{1}{2}} e^{-t} d t=\Gamma\Big(\frac{1}{2}\Big)
$$

### Fórmula per nombres semienters positius

*A partir de la propietat $\Gamma(z+1)=z\Gamma(z)$ s’observa que*

$$
\Gamma(n+1/2)=\frac{(2n-1)!!}{2^n}\Gamma(1/2)
$$

*I coneixent el valor de $\Gamma(\frac{1}{2})$, la fórmula per semienters positius queda*

$$
\boxed{\Gamma(n+1/2)=\frac{(2n-1)!!}{2^n}\sqrt{\pi}}
$$

> *On $!!$ denota el [doble factorial](https://math.fandom.com/wiki/Double_factorial) del nombre enter $(2n-1)$.*
> 
- *Expressió alternativa*
    
    *A partir de la identitat següent*
    
    $$
    (2 k-1) ! !=\frac{(2 k) !}{2^k k !}
    $$
    
    *Podem reescriure l’expressió sense involucrar dobles factorials*
    
    $$
    \Gamma(n+1/2)=\frac{(2 n) !}{4^n n !} \sqrt{\pi}
    $$
    

---

### Extra: Valors concrets més avançats

*Nota: les següents són constants transcendentals i independents algebraicament de $\pi$*

$$
\Gamma\Big(\frac{1}{3}\Big)\qquad
\Gamma\Big(\frac{1}{4}\Big)\qquad
\Gamma\Big(\frac{1}{5}\Big)\qquad
\Gamma\Big(\frac{2}{5}\Big)\qquad
\Gamma\Big(\frac{1}{8}\Big)
$$

- *Valors numèrics aproximats*
    - $\Gamma(\frac{1}{3})\approx
    2.6789$
    - $\Gamma(\frac{1}{4})\approx
    3.6256$
    - $\Gamma(\frac{1}{5})\approx
    4.5908$
    - $\Gamma(\frac{1}{8})\approx
    7.5339$
    - $\Gamma(\frac{2}{5})\approx
    ~????$

*Alguns valors concrets per $p/q\lt 1$*

$$
\begin{aligned}
\Gamma\left(\frac{1}{2}\right) & =\sqrt{\pi} 
& \quad
\Gamma\left(\frac{2}{3}\right) & =\frac{2 \pi}{\Gamma\big(\frac{1}{3}\big)\sqrt{3}} 
\\[1.6em]
\Gamma\bigg(\frac{3}{4}\bigg)
&=\frac{\pi\sqrt{2}}{\Gamma\big(\frac{1}{4}\big)} 
& 
\Gamma\left(\frac{1}{6}\right) & =\frac{\big[\Gamma\big(\frac{1}{3}\big)\big]^2\sqrt{3}}{\sqrt{\pi} 2^{1 / 3}}
\\[1.6em]
\Gamma\left(\frac{3}{5}\right) & =\frac{\pi \sqrt{2} \sqrt{5+\sqrt{5}}}{\Gamma\big(\frac{2}{5}\big)\sqrt{5}}
&
\Gamma\left(\frac{5}{6}\right) & =\frac{\pi^{3 / 2} 2^{4 / 3}}{\big[\Gamma\big(\frac{1}{3}\big)\big]^2\sqrt{3}}
\\[1.6em]
\Gamma\left(\frac{4}{5}\right) & =\frac{\pi \sqrt{2} \sqrt{5-\sqrt{5}}}{\Gamma\big(\frac{1}{5}\big)\sqrt{5}}
& \Gamma\left(\frac{3}{8}\right) & =\frac{\Gamma\big(\frac{1}{8}\big)\sqrt{\pi} \sqrt{\sqrt{2}-1} }{\Gamma\big(\frac{1}{4}\big)}
\\[1.6em]
\Gamma\left(\frac{5}{8}\right) & =\frac{\Gamma\big(\frac{1}{4}\big)}{\Gamma\big(\frac{1}{8}\big)}\sqrt{\pi} 2^{3 / 4}
&
\Gamma\left(\frac{7}{8}\right) & =\frac{\pi 2^{3 / 4} \sqrt{\sqrt{2}+1}}{\Gamma\big(\frac{1}{8}\big)}
\end{aligned}
$$

*Alguns valors concrets per $p/q\gt 1$*

> *A partir de la propietat $\Gamma(z+1)=z\Gamma(z)$ podem calcular més valors*
> 

$$
\begin{aligned}
\Gamma\left(\frac{5}{4}\right) & =\frac{\Gamma\big(\frac{1}{4}\big)}{4}  
& \qquad\quad
\Gamma\left(\frac{7}{4}\right) & =\frac{3\pi\sqrt{2}}{4\Gamma\big(\frac{1}{4}\big)}
\\[1.6em]
\Gamma\bigg(\frac{4}{3}\bigg)
&=~???
& \qquad\quad
\Gamma\left(\frac{5}{3}\right) & =~???
\\[1.6em]
\Gamma\bigg(\frac{6}{5}\bigg)
&=~???
& \qquad\quad
\Gamma\left(\frac{7}{5}\right) & =~???

\end{aligned}
$$

- *Més informació sobre valors particulars de la funció Gamma*
    
    [Particular values of the gamma function](https://en.wikipedia.org/wiki/Particular_values_of_the_gamma_function)
    
    [](https://arxiv.org/pdf/math/0403510v1.pdf)
    

### Extra: Gràfic de la funció Gamma

*Gràfic per valors reals*

[Gamma function](https://www.desmos.com/calculator/hv5gp7dpw7)

*Gràfic per valors complexes*

[DLMF: Figure 5.3.4 ‣ §5.3 Graphics ‣ Properties ‣ Chapter 5 Gamma Function](https://dlmf.nist.gov/5.3.F4.viz)

- *Gràfic interactiu fet amb Plotly*
    
    [https://sympy-plot-backends.readthedocs.io/en/v2.0.1/modules/ccomplex-7.html](https://sympy-plot-backends.readthedocs.io/en/v2.0.1/modules/ccomplex-7.html)
    

## Integrals impròpies relacionades (Integrals Gaussianes)

### Introducció

*En física sovint necessitem calcular les integrals d’aquest tipus de funcions:*

1. $f(x)=x^ne^{-ax}$ 
2. $f(x)=x^ne^{-ax^2}$ 
3. $f(x)=x^n e^{-a(x+b)^2}$
- *A on es fa servir això?*
    
    Física Estadística, Mètodes I, Astro…
    
    *Valor mitjà d’una variable en què la seva densitat decau exponencialment*
    
    $\langle \blue{r}\rangle=\int_{0}^\infty \blue{r}\purple{\rho(r)}dr=
    \int_{0}^\infty \blue{r}\purple{e^{-ar}}dr$
    
    $\langle \blue{r}\rangle=\int_{0}^\infty \blue{r}\purple{\rho(r)}dr=
    \int_{0}^\infty \blue{r}\purple{e^{-ar^2}}dr$
    
    $\langle \blue{x}\rangle=\int_{-\infty}^\infty \blue{x}\purple{\rho(x)}dx=
    \int_{-\infty}^\infty \blue{x}\purple{e^{-ax^2}}dx=0$
    
    $\langle \blue{x^2}\rangle=\int_{-\infty}^\infty \blue{x^2}\purple{\rho(x)}dx=
    \int_{-\infty}^\infty \blue{x^2}\purple{e^{-ax^2}}dx$
    
    > “*Recordem que* $\Delta X=\small\sqrt{\langle X^2\rangle-{\langle X\rangle}^2}$ *i per tant cal saber trobar també $\langle \blue{r^2}\rangle$  i $\langle \blue{x^2}\rangle$ ”.*
    > 
    
    Física Quàntica i Mecànica Quàntica
    
    *Valor esperat d’una variable quan la funció d’ona té un terme que decau exponencialment.*
    
    $\langle \blue{r}\rangle=\int\int\int \Psi^*(r,\theta,\varphi)\blue{r}\Psi(r,\theta,\varphi)dr=C\int_0^\infty [R(r)]^2\blue{r}dr$
    
    > “Acabar de completar-ho un dia més correctament” :)
    > 

### 1. Integral de $x^ne^{-ax}$

*Fent un canvi de variable $t=ax$ obtenim*

$$
\boxed{\int_0^\infty x^ne^{-ax}dx=\frac{\Gamma(n+1)}{a^{n+1}}}

$$

$$
\int_0^\infty x^ne^{-ax}dx=\frac{n!}{a^{n+1}}
$$

- *Procediment canvi de variable*
    
    Canvi de variable: $t=ax\longleftrightarrow x=\frac{t}{a}$
    
    Diferencial: $dt=adx\longleftrightarrow dx=\frac{1}{a}dt$
    
    $$
    \int_0^\infty x^ne^{-ax}dx=\frac{1}{a^{n+1}}\int_0^\infty t^ne^{-t}dt=\frac{\Gamma(n+1)}{a^{n+1}}
    $$
    

*Notar que per aquesta integral **no podem estendre l’interval d’integració**.*

$$
\int_{-\infty}^\infty x^ne^{-ax}dx=\pm\infty
$$

- *Exemples ràpids*
    - $\int_0^\infty e^{-ax}dx=\frac{1}{a}$
    - $\int_0^\infty x^{1/2}e^{-ax}dx=\frac{\sqrt{\pi}}{2\sqrt{a}}$
    - $\int_0^\infty xe^{-ax}dx=\frac{1}{a^2}$
    - $\int_0^\infty x^{3/2}e^{-ax}dx=\frac{3\sqrt{\pi}}{4a^{3/2}}$
    - $\int_0^\infty x^2e^{-ax}dx=\frac{2}{a^3}$
    - $\int_0^\infty x^{5/2}e^{-ax}dx=\frac{15\sqrt{\pi}}{8a^{5/2}}$
    - $\int_0^\infty x^3e^{-ax}dx=\frac{6}{a^4}$

### 2. Integral de $x^ne^{-ax^2}$

*A partir d’un canvi de variable $t=ax^2$ obtenim*

$$
\boxed{\int_0^{\infty} x^n e^{-a x^2} dx=
\frac{\Gamma\big(\frac{n+1}{2}\big)}{2a^{(n+1) / 2}}}

$$

$$
\int_0^{\infty} x^n e^{-a x^2} dx
=
\frac{(n-1)!!}{2^{\frac{n}{2}-1}a^{\frac{n+1}{2}}}\sqrt{\pi}
$$

- *Procediment canvi de variable*
    
    Canvi de variable: $*t=ax^2\longleftrightarrow x=\frac{\sqrt{t}}{\sqrt{a}}$*  
    
    Diferencial: *$dt=2a\frac{\sqrt{t}}{\sqrt{a}}dx=2\sqrt{at}dx\longleftrightarrow dx=\frac{1}{2\sqrt{at}}dt$* 
    
    $$
    \begin{aligned}
    \int_0^{\infty} x^n e^{-a x^2} dx  &= 
    \int_0^{\infty}
    \bigg[\footnotesize\frac{\sqrt{t}}{\sqrt{a}}
    \bigg]^n\normalsize 
    e^{-t} \cdot \frac{1}{2\sqrt{at}}dt
    \\
    &=\frac{1}{2a^{(n+1) / 2}} \int_0^{\infty} t^{\frac{n-1}{2}} e^{-t} d t 
    \\
    &=\frac{1}{2a^{(n+1) / 2}} \Gamma\bigg(\frac{n+1}{2}\bigg)
    \end{aligned}
    $$
    
- *Exemples ràpids*
    - $\int_0^{\infty} e^{-a x^2} dx=
    \frac{\sqrt{\pi}}{2\sqrt{a}}$
    - $\int_0^{\infty} x^{1/2}e^{-a x^2} dx=
    \frac{\pi\sqrt{2}}{2a^{3/4}\Gamma(\frac{1}{4})}$
    - $\int_0^{\infty}x e^{-a x^2} dx=
    \frac{1}{2a}$
    - $\int_0^{\infty}x^{3/2} e^{-a x^2} dx=
    \frac{\Gamma (\frac{1}{4})}{8a^{5/4}}$
    - $\int_0^{\infty}x^2 e^{-a x^2} dx=
    \frac{\sqrt{\pi}}{4a^{3/2}}$
    - $\int_0^{\infty}x^3 e^{-a x^2} dx=
    \frac{1}{2a^2}$
    - $\int_0^{\infty}x^4 e^{-a x^2} dx=
    \frac{3\sqrt{\pi}}{8a^{5/2}}$

*En aquest cas la funció presenta simetria i per tant **podem estendre l’interval d’integració**.*

- *Repàs de paritat de funcions*
    
    *Les següents funcions presenten simetria parell (EVEN) o senar (ODD).*
    
    - $e^{-x^2}=\text{EVEN}$
    - $xe^{-x^2}=\text{ODD}$
    - $x^2e^{-x^2}=\text{EVEN}$
    - $x^3e^{-x^2}=\text{ODD}$
    
    *Per aquests funcions es compleix*
    
    - $\int_0^\infty \text{EVEN}=2\int_{-\infty}^{\infty}\text{EVEN}$
    - $\int_{-\infty}^\infty \text{ODD}=0$
    
    *Per més informació entrar a* [Paritat de funcions](https://www.notion.so/Paritat-de-funcions-367770bf2bb04dbeb93dd4cf21c5e7a2?pvs=21) 
    

*Per $n$ senar*

$$
\boxed{\int_{-\infty}^\infty x^ne^{-ax^2}=0}
$$

*Per $n$ parell*

$$
\boxed{
\int_{-\infty}^{\infty} x^n e^{-a x^2} dx
=
\frac{\Gamma\left(\frac{n+1}{2}\right)}{a^{(n+1) / 2}}}
$$

$$
\int_{-\infty}^\infty x^ne^{-ax^2}=
\frac{(n-1)!!}{2^{\frac{n}{2}}a^{\frac{n+1}{2}}}\sqrt{\pi}
$$

- *Exemples ràpids*
    - $\int_{-\infty}^{\infty} e^{-a x^2} dx=
    \frac{\sqrt{\pi}}{\sqrt{a}}$
    - $\int_{-\infty}^{\infty}x e^{-a x^2} dx=0$
    - $\int_{-\infty}^{\infty}x^2 e^{-a x^2} dx=
    \frac{\sqrt{\pi}}{2a^{3/2}}$
    - $\int_{-\infty}^{\infty}x^3 e^{-a x^2} dx=
    0$
    - $\int_{-\infty}^{\infty}x^4 e^{-a x^2} dx=
    \frac{3\sqrt{\pi}}{4a^{5/2}}$

### 3. Integral de $x^ne^{-(ax^2+bx+c)}$

*Per resoldre aquesta integral ens anirà bé fer un repàs sobre la distribució Gaussiana, també anomenada distribució normal.*

- *Repàs distribució Gaussiana*
    
    *La distribució gaussiana o distribució normal té com a expressió:*
    
    $$
    f(x)=\frac{1}{\sigma \sqrt{2 \pi}} e^{-\frac{1}{2}\left(\frac{x-\mu}{\sigma}\right)^2}=n(\mu,\sigma^2)
    $$
    
    *En què $\mu$ és el valor mitjà de la variable i $\sigma$ és la anomenada desviació estàndard.* 
    
    *Per no allargar-se aquí explicant el significat estadístic d’aquests paràmetres ni el d’on surt l’expressió, deixarem un fragment de 2 minuts d’un [vídeo](https://www.youtube.com/watch?v=zeJD6dqJ5lo&t=6s) de 3Blue1Brown que ho explica.*
    
    - *Vídeo explicació 3Blue1Brown*
        
        [normal distribution 3b1b.mp4](Funcio%CC%81%20gamma%20i%20integrals%20Gaussianes%20a36b737c30724e5fa94773df96954468/normal_distribution_3b1b.mp4)
        
    
    *Molt bé, la distribució normal (com qualsevol funció realment) té uns [moments](https://en.wikipedia.org/wiki/Normal_distribution#Moments) (matemàtics) associats. Per la distribució normal aquests moments són*
    
    $$
    %----- CONFIGURACIÓ ------
    \def\arraystretch{1.5}
    \small
    %-------------------------
    
    \begin{array}{|c|c|c|c|}
    \hline
    %--- FILA 1 ---
    \textbf{Ordre} 
    & 
    \textbf{Moment no central}
    &
    \textbf{Moment central}
    &
    \pmb{\mathbb{E}[x^n]}
    %-------------- 
    \\ \hline
    %--- FILA 2 ---
    1
    & 
    \mu
    &
    0
    &
    0
    %--------------
    \\ \hline
    %--- FILA 3 ---
    2
    & 
    \mu^2+\sigma^2
    &
    \sigma^2
    &
    1
    %--------------
    \\ \hline
    %--- FILA 4 ---
    3
    & 
    \mu^3+3\mu\sigma^2
    &
    0
    &
    0
    %--------------
    \\ \hline
    %--- FILA 5 ---
    4
    & 
    \mu^4+6\mu^2\sigma^2+3\sigma^4
    &
    3\sigma^4
    &
    3
    %--------------
    \\ \hline
    \end{array}
    $$
    
    *Nota: quan a la pàgina de [FONLAB](https://www.notion.so/FONLAB-8f89885297f447dc8c736c4220fa494a?pvs=21) estigui més completada i això estigui explicat bé i al detall allà, simplement referenciar-la.*
    
    *Més informació:*
    
    $$
    E\left([X-\mu]^k\right)=\mu_k=\int_{-\infty}^{\infty}(x-\mu)^k P(x) \mathrm{d} x
    $$
    
    $$
    M(t)=E\left(\mathrm{e}^{t X}\right)=\int_{-\infty}^{\infty} \mathrm{e}^{t x} P(x) \mathrm{d} x
    $$
    
    [Moment Generating Function of Gaussian Distribution - ProofWiki](https://proofwiki.org/wiki/Moment_Generating_Function_of_Gaussian_Distribution)
    

*Bé, doncs la gràcia està en adonar-se que podem expressar $e^{-ax^2+bx}$ com una distribució normal si considerem $\mu=\frac{b}{2a}$ i $\sigma=\frac{1}{2a}$.*

- *Procediment*
    
    $$
    n(\mu,\sigma^2)
    =\frac{1}{\sigma \sqrt{2 \pi}} e^{-\frac{1}{2}\left(\frac{x-\mu}{\sigma}\right)^2}=\frac{2a}{ \sqrt{2 \pi}} e^{-\frac{1}{2}\left(\frac{x-b/2a}{2a}\right)^2}=tal
    $$
    

$$
e^{-a x^2+b x}=\Bigg[\sqrt{\frac{\pi}{a}} e^{\frac{b^2}{4 a}}\Bigg]  n(\mu,\sigma^2)
$$

*I això permet resoldre la integral en funció dels moments d’una distribució normal estàndard*

$$
\int_{-\infty}^{+\infty} x^n e^{-a x^2+b x} d x=\sqrt{\frac{\pi}{a}} e^{\frac{b^2}{4 a}} \int_{-\infty}^{+\infty} x^n n\left(\mu, \sigma^2\right) d x=\sqrt{\frac{\pi}{a}} e^{\frac{b^2}{4 a}} \mathbb{E}\left[x^n\right]
$$

*Si aquí hi afegim la constant $e^{-c}$ que ens faltava, l’expressió queda*

$$
\boxed{\int_{-\infty}^{+\infty} x^n e^{-(a x^2+b x+c)} 
d x=\sqrt{\frac{\pi}{a}} e^{\left(\frac{b^2}{4 a}-c\right)} \mathbb{E}\left[x^n\right]}
$$

*Ara bé, no és trivial (veure el repàs per més informació), ja que depèn de la [funció error](https://en.wikipedia.org/wiki/Error_function), de fet depèn de la funció error complementària, que per $n=0$ pren el valor de $1$, però per $n\ge1$ no hi ha solució analítica (crec).*

$$
\mathbb{E}[x^0]=1\qquad
\mathbb{E}[x^n]=\begin{cases}
0\quad &n\text{ senar}\\
(n-1)!!\quad& n\text{ parell}\ge2
\end{cases}
$$

Valors particulars

$$
\boxed{\int_{-\infty}^{\infty}e^{-(ax^2+bx+c)}dx=\small\sqrt{\frac{\pi}{a}}\normalsize e^{\frac{b^2-4ac}{4 a}}}
$$

$$
\boxed{\int_{-\infty}^{\infty} x e^{-\left(a x^2+b x+c\right)} d x=\frac{b}{2 a} \sqrt{\frac{\pi}{a}}e^{\frac{b^2-4ac}{4 a}}}
$$

- Extra
    
    $$
    \int_0^\infty x^n e^{(ax^2+bx)}dx
    $$
    
    L*’expressió resultant d’integrar per parts:*
    
    $$
    \int_{-\infty}^{\infty} e^{-a(x+b)^2} d x=\frac{1}{4}\sqrt{\frac{\pi}{a}}
    $$
    
    És a dir que no depèn de $b$, això és així ja que el paràmetre només desplaça la funció, no la deforma. Tal com es pot observar en el gràfic.
    

### Info

> “All normal distribution can be transformed into standard normal distribution
by centralized and normalized the random variable by the formula:”
> 

$$
Z_n=\frac{X_n-\mu}{\sigma}
$$

> “As mentioned above, the sequence of moments (starting from order 1 moment)
of a normal distribution when calculated has the pattern: {μ, μ2 + σ2, μ3 + 2μσ, μ4 +
6μ2σ2 + 3σ4, μ5 + 10μ3σ2 + 15μσ4, μ6 + 15μ4σ2 + 45μ2σ4 + 15σ6, μ7 + 21μ5σ2 + 105μ3σ4 +
105μσ6, μ8 + 28μ6σ2 + 210μ4σ4 + 420μ2σ6 + 105σ8, ...”
> 

> “Thus, for a standard normal distribution, its moment sequence (starting from order
1 moment) is always: {0,1,0,3,0,15,0,105,...} (subtituting σ = 1 and μ = 0 into the
sequence above”
>