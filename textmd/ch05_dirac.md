TODO: intro

# Complex Klein-Gordon Waves: Charge!

We have mentioned that a major problem with the scalar KG equation developed so far is that it doesn't represent any kind of conserved value: you cannot compute some constant, unchanging value from the $\varphi$ state variables under this equation. Why is this a problem? If you want to develop a probabilistic interpretation of the wave, as in Schrödinger's equation, then you need this. But the conserved value that emerges naturally from the KG equation comes with two different signs, positive and negative, whereas Schrödinger's equation always produces a positive value. This is one of the major reasons why the KG equation is not widely discussed in quantum physics: it doesn't quite fit with the standard probabilistic framework.

Instead, it seems to make much more sense to interpret the KG waves as **waves of charge**, because charge is also strictly conserved, and it comes in both positive and negative varieties. Indeed, the authors that do write extensively about the KG equation adopt this interpretation (Greiner, 2000; Gingrich, 2004; Mandl and Shaw, 1984). Furthermore, we will see that this charge interpretation fits naturally with the coupling of this KG equation to the electromagnetic field, where the conserved charge value acts just like the electric charge in driving the field. Interestingly, this idea was pursued initially by Schrödinger in 1926, and has been pursued more recently in neoclassical self-coupled field theory (Jaynes & Cummings, 1963; Crisp & Jaynes, 1969; Barut & Van Huele, 1985; Barut & Dowling, 1990; Crisp, 1996; Finster, Smoller & Yau, 1999c; Radford, 2003; Masiello, Deumens & Ohrn, 2005). We discuss this approach, which is essentially an analytic version of our computational model, in more detail later.

Our emerging picture of a particle is therefore that it is a distributed wave-packet of charge that flows through space according to some variant of the KG equation. This conflicts with the standard view that charge is contained within single discrete point particles, that somehow float around in clouds of moving probability waves. Indeed, even such a quasi-mechanistic view is too strong for the classical Copenhagen interpretation of quantum physics, which says that the particles simply do not have any definite existence until they are measured by some kind of measuring device. We return to such issues later.

Now, let's see how we can get this conserved charge value out of a KG equation. Fortunately it is quite simple, and somewhat magical. By just computing the same basic KG equation on a complex state variable ($\phi$) instead of a scalar state variable ($\varphi$), a conserved quantity emerges. The magic of this result is magnified by the fact that, as a second order wave equation without an $i$ term, the KG equation on a complex variable is identical to just computing two separate KG equations on each of the two scalar values represented by the complex state variable (i.e., $\varphi_a$ and $\varphi_b$). Note that this was not true of Schrödinger's wave equation, which is first order and has an $i$ term that causes the $a$ and $b$ terms to intermix as the wave unfolds.

To be explicit, the KG wave equation for a complex state variable $\phi$ is:

- $\frac{\partial^2 \phi}{\partial t^2} = (\nabla^2 - m_0^2) \phi $

and, because differentiation operates independently on the two separate scalar variables in a complex number, this is equivalent to two parallel scalar KG equations, which we can write as:

- $\frac{\partial^2 \varphi_a}{\partial t^2} = \left( \nabla^2 - m_0^2 \right) \varphi_a $
- $\frac{\partial^2 \varphi_b}{\partial t^2} = \left( \nabla^2 - m_0^2 \right) \varphi_b $

where again the $\varphi_a$ indicates a scalar state variable representing the real $a$ component of $\phi$, and $\varphi_b$ represents the imaginary $b$ value.

Ok, so how do you get a charge out of that, so to speak? As with Schrödinger's equation, the procedure involves multiplying by the complex conjugate ($\phi^\* = \varphi_a - i \varphi_b$), which generally produces the overall magnitude or length of the vector represented by the two components of the complex number: $\varphi_a^2 + \varphi_b^2$. As the derivation presented in detail in Appendix B shows, if you compute the sum of this value across all of space (actually an integral, using continuous equations), and set it equal to zero (so that it never changes), you end up with an expression for the density and motion (current) of a quantity that is conserved (i.e., the charge).

The resulting expression for computing the density of charge (typically written as $\rho$, which is the Greek letter "rho"), which is to say, the amount of charge per cubic state unit, is:

- $\rho \equiv \frac{i \hbar e}{2m_0c^2} \left( \phi^\* \frac{\partial \phi}{\partial t} - \phi \frac{\partial \phi^\*}{\partial t} \right) $

where the $e$ value is a constant (.0787??) that converts natural units into proper units of charge.

This can be expressed in terms of the underlying scalar state variables that make up the complex state ($\phi = \varphi_a + i \varphi_b$), and their first temporal derivatives ($\dot \varphi_a$ and $\dot \varphi_b$), and using natural units where $c=\hbar=1$, as:

- $\rho_i = \frac{e}{m_0} ({\varphi_b}\_i \dot {\varphi_a}\_i - {\varphi_a}\_i \dot {\varphi_b}\_i) $

This is directly computable for each cubic cell $i$ in the system.

It becomes very clear when explicitly written out in this manner that charge represents a coupling of the two otherwise independent variables in the complex number, and this suggests why a single scalar number cannot represent a conserved charge value. The fact that these variables are coupled here, but not in the actual wave equations that drive their updating, seems magical.

Perhaps the most important feature of this equation is that it can be either positive or negative. For example, if ${\varphi_a}\_i \dot {\varphi_b}\_i$ happens to be larger than ${\varphi_b}\_i \dot {\varphi_a}\_i$ (and there is nothing preventing this from being the case), then it will be negative. This is not true of the corresponding expression for Schrödinger's equation, which is "definitely positive", or, in mathematical terminology, "positive definite". As noted earlier, this is one of the major reasons why standard quantum physics has strongly embraced Schrödinger's equation, and not KG: KG does not fit with the standard probabilistic framework, where the wave describes a probability, and a probability is always positive.

Interestingly, the Dirac equation, which standard physics has adopted as a model of the electron (and we'll cover later), also produces negative "probabilities", but these have been (correctly, in our framework) reinterpreted as representing antiparticles (i.e., particles with an opposite charge). The antiparticle of the electron is the **positron**, and it is just like an electron, except it has the opposite charge. Historically, this antiparticle nature of the Dirac equation was regarded as a major problem, until positrons were subsequently discovered, and then Dirac looked like a genius for having made such a bold prediction. Nevertheless, there seems to be some residual discomfort in all this, and many treatments of quantum electrodynamics marginalize the Dirac equation in favor of a largely particle-based treatment. We return to these issues later.

`\begin{figure}`
` \centering\includegraphics[height=2in]{fig.vgrad.eps}`  
` \caption{\small The gradient of a scalar field ({{< math >}}\vec{\nabla}{{< /math >}}), which`  
`   produces a vector field describing the slope at each point in space.`  
`    These gradient vectors point in the direction of maximum ``downhill''`
`   slope.  In this example the scalar field is a circularly-symmetric bump.}`  
` \label{fig.vgrad}`
`\end{figure}`

We can also derive an expression for the motion charge over space, which is the *charge current density* $\vec{J}$:

- $\vec{J} \equiv - \frac{i \hbar e}{2m_0} \left( \phi^\* \vec{\nabla} \phi - \phi \vec{\nabla} \phi^\* \right) $

In terms of the underlying scalar state variables (and again for natural units), this is:

- $\vec{J} = \frac{e}{m_0} (\varphi_a \vec{\nabla} \varphi_b - \varphi_b \vec{\nabla} \varphi_a) $

This value indicates how much charge is moving in each of the three different coordinate directions; the $\vec{}$ symbol on top of $\vec{J}$ indicates that this is a vector, containing a separate real scalar value for each direction: $\vec{J} = (J_x, J_y, J_z)$. As noted earlier the $\vec{\nabla}$ symbol is the vector gradient operator, which computes the rate of change of the values along each dimension:

- $\vec{\nabla} \equiv \left(\frac{\partial}{\partial x}, \frac{\partial}{\partial y}, \frac{\partial }{\partial z}\right) $

This just means that this $\vec{\nabla}$ takes a three-dimensional field, in this case the field of our wave value $\varphi_a$ or $\varphi_b$ distributed over space, and computes how steeply this field is changing in each of the three different directions (Figure~\ref{fig.vgrad}). If we assume that this value is actually computed in our model, then we'll need a way of computing the gradient $\vec{\nabla}$ in discrete space-time. This is covered in the next section.

Before proceeding, we look ahead to the next major development. We have ways of computing the density and current of charge ($\rho$, $\vec{J}$), which drive the electromagnetic field. Thus, we need to think of these variables as physically real values, which can be computed directly from the underlying wave state variables, that give rise to long-range electromagnetic forces, through which our particle-waves interact. The next step is to see how the electromagnetic fields can push our particle waves around.

See [Discrete Gradient](ch03_em.md) for how to compute the gradient in the discrete CA framework.

So, in the end, the computation of the current, which is a vector having three separate components ($J_x, J_y, J_z$), looks like this:

- $J_x = \frac{e}{m_0} \left\[ \varphi_a \left( \sum\_{j \in N\_{X}} k_j {(\varphi_b}\_{j+} - {\varphi_b}\_{j-}) \right) - \varphi_b \left( \sum\_{j \in N\_{X}} k_j ({\varphi_a}\_{j+} - {\varphi_a}\_{j-}) \right) \right\] $
- $J_y = \frac{e}{m_0} \left\[ \varphi_a \left( \sum\_{j \in N\_{Y}} k_j ({\varphi_b}\_{j+} - {\varphi_b}\_{j-}) \right) - \varphi_b \left( \sum\_{j \in N\_{Y}} k_j ({\varphi_a}\_{j+} - {\varphi_a}\_{j-}) \right) \right\] $
- $J_z = \frac{e}{m_0} \left\[ \varphi_a \left( \sum\_{j \in N\_{Z}} k_j ({\varphi_b}\_{j+} - {\varphi_b}\_{j-}) \right) - \varphi_b \left( \sum\_{j \in N\_{Z}} k_j ({\varphi_a}\_{j+} - {\varphi_a}\_{j-}) \right) \right\] $

Again, it does not look as simple as before, but nevertheless it is necessary to have a current to be able to drive the magnetic field in an manner consistent with known physics. Specifically, as we saw earlier, the electromagnetic field equations require both $\rho$ and $\vec{J}$ values as their sources. In addition, this gradient operation is necessary for several other computations in our model, so, like the laplacian, it can be thought of as one of just a few basic operations that take place over the neighborhood of cells.

# Minimal Coupling of Charge Waves with Electromagnetic Fields

At this point, we have a charged wave that can generate an electromagnetic field according to the charge density $\rho$ and current density $\vec{J}$, and we know how this electromagnetic field propagates according to wave equations. Now, we need to have that electromagnetic field interact with the charge wave to produce actual forces on our model \`\`particles*. This occurs by introducing new terms into the complex KG wave equation, which, intuitively speaking, act as external \`\`driving forces* on this charge wave, in much the same way that the charge and current act as driving forces on the electromagnetic wave equations.

In the electromagnetic field equations, the driving force from charge $\rho$ adds into the second-order temporal derivative $\frac{\partial^2 {}}{\partial t^2}$ (equation~\ref{eq.em_pot_wv}):

- $\frac{\partial^2 {A_0}}{\partial t^2} = \nabla^2 A_0 + \frac{1}{\epsilon_0} \rho $

However, in Schrödinger's equation, external forces enter as a potential ($V$), in the first-order derivative  $\frac{\partial {}}{\partial t}$:

- $i \hbar \frac{\partial {\phi}}{\partial t} = \frac{\hbar^2}{2m} \nabla^2 \phi + V \phi $

This makes sense, because force is the derivative of a potential, so potential is a first-order factor, and force is a second-order factor.

Our KG (Klein-Gordon) charge wave equation is a second-order equation, expressed in terms of $\frac{\partial^2 {}}{\partial t^2}$, and therefore we need to include external driving forces, not potentials. However, for various reasons, it is necessary to derive such an equation starting from the potential. To do this, we can re-derive a second-order wave equation by replacing the first-order derivative with the first-order derivative with the external driving potential:

- $\partial^\mu \rightarrow \partial^\mu - \frac{e}{c} {A}^\mu $

We can then substitute this first-order four-vector derivative into the four-vector version of the KG wave equation (in natural units), which is (equation~\ref{eq.kg_4vm}):

- $\partial\_\mu \partial^\mu \phi = - m_0^2 \phi $

because, as we've noted before (equation~\ref{eq.covgrcongr}):

- $\partial\_\mu \partial^\mu = \frac{\partial^2 {}}{\partial t^2} - \nabla^2 $

So the compact form of the KG wave equation with minimal coupling is therefore:

- $\left( \partial\_\mu - e {A}\_\mu \right) \left(\partial^\mu - e {A}^\mu \right) \phi = -m_0^2 \phi $

To get all the units right, and perhaps add some conceptual clarity, we can do the same thing with the four-momentum version of the wave equation (equation~\ref{eq.kg_p4v}), which is:

- $\hat{p}^\mu \hat{p}\_\mu \phi = m_0^2 c^2 \phi $

where the momentum operator is essentially just the four-derivative, plus the pesky $i$ and $\hbar$ factors (equation~\ref{eq.4p}):

- $\hat{p}^\mu = i \hbar \partial^\mu $

So now we can say that the electromagnetic potential pushes directly on the momentum of the wave-particle:

- $\hat{p}^\mu \rightarrow i \hbar \partial^\mu - \frac{e}{c} {A}^\mu $

and the same goes for the covariant forms:

- $\hat{p}\_\mu \rightarrow i \hbar \partial\_\mu - \frac{e}{c} {A}\_\mu $

This notion of the potential pushing directly on the momentum of the particle hopefully makes good intuitive sense, even if all the associated mathematics does not. In any case, the resulting KG wave equation becomes:

- $\left({\hat{p}^\mu} - \frac{e}{c}{A}^\mu \right) \left({\hat{p}\_\mu} - \frac{e}{c}{A}\_\mu \right)\phi = m_0^2 c^2 \phi $

which can also just be written more compactly as a squared expression:

- $\left(i \hbar \partial\_\mu - \frac{e}{c}{A}\_\mu \right)^2\phi = m_0^2 c^2 \phi $

When this equation is crunched through to produce separate time and space derivatives (as detailed in a subsequent section), we get a standard second-order wave update equation plus a few extra terms (in natural units):

- $\frac{\partial^2 {\phi}}{\partial t^2} = \nabla^2 \phi - m_0^2\phi - 2 i e \left(A_0 \frac{\partial {\phi}}{\partial t} + \vec{A} \cdot \vec{\nabla} \phi \right) + e^2 \phi \left(A_0^2 - \vec{A}^2\right) $

Including all of the various constants, it is:

- $\frac{\partial^2 {\phi}}{\partial t^2} = c^2 \left( \nabla^2 - \frac{m_0^2 c^2}{\hbar^2} \right) \phi - \frac{2 i e}{\hbar} \left(A_0 \frac{\partial {\phi}}{\partial t} + c \vec{A} \cdot \vec{\nabla} \phi \right) + \frac{e^2 \phi}{\hbar^2} \left(A_0^2 - \vec{A}^2\right) $

This equation amounts to the basic KG wave equation, plus terms that involve the interaction between the charge wave and the electromagnetic field potentials $A_0$ and $\vec{A}$. For example, in the second term of this equation, the vector potential $\vec{A}$ "pushes" on the gradient of the wave function $\vec{\nabla} \phi$, and the scalar potential $A_0$ pushes on the temporal derivative $\frac{\partial {\phi}}{\partial t}$. Notice that these interactions are all first-order, in terms of the potentials and first-order derivatives of the wave equations. The second-order electromagnetic force fields $\vec{E}$ and $\vec{B}$ do not appear at all! This is despite the fact that these are widely regarded as the primary observables of electromagnetic force. Also, the electromagnetic terms introduce a coupling between the two components of the complex variable $\phi$, because of the presence of the imaginary number $i$ in this term. Therefore, it is only the "free" particle (without electromagnetic forces) that has the completely uncoupled scalar components.

Before we pause to reflect more, we need to take two more steps. First, because $\phi$ is a complex variable, we need to further compute the separate real-valued update equations for $\varphi_a$ and $\varphi_b$ to simulate this in our model. Second, we need to update the charge and current equations for this new version of the KG wave equations.

The resulting CA model update equations (including all the relevant $c$ and $\hbar$ factors) are:

- $\ddot \varphi_a^{t+1} = c^2 \left(\nabla^2 \varphi_a - \frac{m_0^2c^2}{\hbar^2} \varphi_a \right) + \frac{2 e}{\hbar} \left(A_0 \dot \varphi_b + c \vec{A} \cdot \vec{\nabla} \varphi_b \right) + \frac{e^2}{\hbar^2} \varphi_a \left(A_0^2 - \vec{A}^2 \right) $

and:

- $\ddot \varphi_b^{t+1} = c^2 \left(\nabla^2 \varphi_b - \frac{m_0^2c^2}{\hbar^2} \varphi_b \right) - \frac{2 e}{\hbar} \left(A_0 \dot \varphi_a + c \vec{A} \cdot \vec{\nabla} \varphi_a \right) + \frac{e^2}{\hbar^2} \varphi_b \left(A_0^2 - \vec{A}^2 \right) $

(where for simplicity the right hand side variables are implicitly taken at time $t$ for cell $i$, and the discrete versions of $\nabla^2$ and $\vec{\nabla}$ presented earlier are assumed). Note that we again need the first-order spatial gradient operator $\vec{\nabla}$ as a basic computation in our model, but otherwise all the variables are local to the system.

The conserved charge and current values computed by this equation must also be updated. The coupling with the electromagnetic field has introduced additional factors here, which depend on the electromagnetic potentials $A_0$ and $\vec{A}$. For the charge density $\rho$, we have:

- $\rho = \frac{i \hbar e}{2m_0c^2} \left( \phi^\* \frac{\partial {\phi}}{\partial t} - \phi \frac{\partial {\phi^\*}}{\partial t} \right) - \frac{e^2}{m_0 c^2} A_0 \phi \phi^\* $

If you compare with the original charge equation for the complex KG equation (equation~\ref{eq.charge}), it is the same except for the last term. Similarly, the current density $\vec{J}$ is:

- $\vec{J} \equiv - \frac{i \hbar e}{2m_0} \left( \phi^\* \vec{\nabla} \phi - \phi \vec{\nabla} \phi^\* \right) - \frac{e^2}{m_0 c} \vec{A} \phi \phi^\* $

again with an extra term at the end relative to equation~\ref{eq.current}.

These equations need to be converted into computational expressions in terms of the separate complex components, as before:

- $\rho = \frac{\hbar e}{m_0c^2} (\varphi_b \dot \varphi_a - \varphi_a \dot \varphi_b) - \frac{e^2}{m_0 c^2} A_0 (\varphi_a^2 + \varphi_b^2) $
- $\vec{J} = \frac{\hbar e}{m_0} (\varphi_a \vec{\nabla} \varphi_b - \varphi_b \vec{\nabla} \varphi_a) - \frac{e^2}{m_0c} \vec{A} (\varphi_a^2 + \varphi_b^2)$

At this point, we have reached an important milestone --- if you take the equations just presented above, this describes a particle as a distributed wave of charge that gets pushed around by the electromagnetic field potentials ($A_0$ and $\vec{A}$). Furthermore, this wave of charge produces electromagnetic fields, in terms of charge and current densities $\rho$ and $\vec{J}$. Thus, we finally have a complete system of equations that can potentially simulate charged particles whizzing around and interacting with each other. In other words, we finally have the potential to make direct contact with observable physics! Indeed, you can explore the behavior of this system in the model, by using the Complex Coupled KG wave equations setting.

# Numerical Issues with Coupling: Symmetry Breaking

When you actually simulate these equations on the computer, something very interesting (and initially distressing) happens --- they blow up! As you run the equations over time in the presence of a fixed electromagnetic field, the total charge value, far from being a constant, increases steadily, and eventually you end up with numbers approaching infinity. This is not because the math is wrong (after very thorough checking!), but because of the coupling between the two elements of the complex variable that occurs in the update equation. Specifically, the update of $\varphi_a$ depends on $\dot \varphi_b$ and $\vec{\nabla} \varphi_b$, and vice-versa. This interdependency creates numerical instabilities when we simply substitute in the discrete computed values at each time step. In particular, because the change in $\varphi_a$ depends on the change in $\varphi_b$, this cycle of dependency can get out of whack.

Intuitively, the electromagnetic potentials drive a rotation through the $\varphi_a$ and $\varphi_b$ variables, which is evident in the fact that they subtract from $\varphi_b$ but add to $\varphi_a$ --- these opposite signs are the signature of a rotation (and incidentally are caused by the presence of the imaginary $i$ numbers in the equations). To the extent that the potentials are pushing the $\varphi_a$ variable up, there should be an equal and opposite pushing of the $\varphi_b$ variable down, causing the rotation. However, if the $\varphi_b$ variable only has the "old" data from the previous time step about how much $\varphi_a$ got pushed up, then it doesn't compensate correctly in how much it gets pushed down. Thus, you end up with a "leak" in the system, where instead of rotating nicely in place, the system starts to fly out of control, spinning wider and wider circles each time.

The solution to this problem is to *break the symmetry* between $\varphi_a$ and $\varphi_b$ in these update equations. Instead of updating each of them at the same time, based on the prior values of the other, we choose one variable ($\varphi_a$, arbitrarily) and update its values first. Then, when we compute $\varphi_b$, we use the {\em current value} of $\dot \varphi_a$ in the update equation for $\varphi_b$. This prevents the rotation between these variables from getting out of whack, and restores numerical stability to the system. % todo: run KG invr5 case, plot figure!

`\begin{figure}`
` \centering\includegraphics[height=2in]{fig.dirac_invr5_50.eps}   \caption{\small Total charge for updating of the charge wave     equation over 100,000 time steps in the presence of a fixed {{< math >}}1/r{{< /math >}}     potential with magnitude .5, in a universe of {{< math >}}50^3{{< /math >}} cubes.  The`  
`   instantaneous total charge varies considerably over time, but the average     across time is constant, demonstrating that total charge is conserved on     average, but not at each moment.  If no potential is present, then charge     is identically conserved from one time step to the next.}`  
` \label{fig.kg_invr5_50} \end{figure}`

However, if you run this equation in a static electromagnetic field, it is clear that the total amount of charge in the model at any one time changes over time (Figure~\ref{fig.kg_invr5_50}). This is flies in the face of the fancy math that says that these equations conserve charge! Somewhat amazingly, however, if you run the system long enough, it becomes clear that the _average_ amount of charge never changes.

Overall, we have now happened upon a very interesting situation. The breaking of symmetry between the two variables in the complex wave state, forced upon us by implementational considerations, actually fits at least qualitatively with a known and otherwise very puzzling property of physics. The weak force also breaks symmetry in a very similar way: there is a preferred direction of rotation in the weak force. Although it is not yet clear (to me at least) that this preferred rotational direction in the weak force maps identically onto this preferred rotation direction, it is nevertheless a tantalizing possibility. The weak force has been integrated with the electromagnetic force, as the _electroweak_ force --- it is possible that the effects described by the electroweak force correspond in some way to the oscillations in charge value that are observed in our model. We will return to these issues later.

Meanwhile, we nee need to introduce just a bit more complexity into our KG wave equation before we have a fully satisfactory model of a fundamental particle of nature: the electron (and its antiparticle, the positron). This extra bit of complexity extends the phenomenon of rotation that we've just been discussing, to account for the strange quantum mechanical property of **spin**. The resulting equation goes by the name of the second-order Dirac equation. Once we have that, we will have a complete system that, if all the math is correct, should make direct and numerically accurate contact with observable phenomena!

Before moving on to spin, there are two remaining loose ends for the present set of equations. First, there is an interesting interpretation of the way that the electromagnetic potential interacts with our charge wave, called **local gauge invariance**, which provides a template for exploring the other two forces of nature: the weak and strong forces (which we will not cover further in this paper). Second, we have the actual mechanics of deriving the above equations.

# Local Gauge Invariance

If you look at it in the right way, the electromagnetic field can be seen as a way of canceling out an extra degree of freedom present in the complex KG wave field equations. As we mentioned earlier, the Lorenz gauge is an example of a situation where we introduced some extra constraints on the field variables, and this eliminated a degree of freedom in the electromagnetic equations, and also made them appear a lot simpler than they otherwise would. This notion of a *gauge* is very general: it just means that whenever you have some unconstrained values in your equations (i.e., values that can change without changing the observable results that you can measure in physics experiments), then you need to apply some kind of gauge to fix these variables. In the Lorenz gauge example, the extra degree of freedom comes from the fact that the observable variables are the force vectors $\vec{E}$ and $\vec{B}$, which are essentially derivatives of the underlying potentials $A_0$, $\vec{A}$. Thus, the raw values of the potentials can be moved up or down, and it won't change the slope of the fields, and therefore it won't change the observable force vectors. However, it is not clear exactly how to reconcile such an argument with the fact that the potentials appear directly in our coupling equations, and also are observable in terms of the Arahnov-Bohm effect, as discussed elsewhere.

Nevertheless, here is the argument for the electromagnetic coupling being a form of local gauge invariance. If you just take our basic complex KG wave equation, you can get exactly the same overall behavior if you multiply the thing by a "phase transformation" (it is often said that gauge invariance should really be phase invariance) which is basically just a rotation along the complex axes. This is exactly the kind of rotation discussed above. The generic form of a rotation in complex numbers is to multiply by an exponential term:

- $\phi(x) \rightarrow \exp \left(\frac{ie}{\hbar c} \chi \right) \phi(x) $

Where the $\chi$ term is the amount that you're rotating (the rest are just convenient constants for getting $\chi$ into the right units) --- think of it as some number of degrees of rotating the underlying $\varphi_a$ value into $\varphi_b$ (and vice-versa) for the complex number $\phi$.

If $\chi$ is independent of location ($x$), then it is just a constant and nothing happens. This is a *global* gauge/phase transformation, and it is not very interesting. However, if $\chi$ is now itself a function of location (i.e., $\chi(x)$ ), this is a *local* gauge transformation, and this is where the electromagnetic coupling comes in. If you have such a local variable, and you take the derivative of the resulting overall system that includes this locally-varying thing, you get this extra term for the derivative of $\chi(x)$ with respect to x:

- $\partial\_\mu \phi(x) \rightarrow \exp \left( \frac{ie}{\hbar c} \chi(x) \right) \left(\partial\_\mu + \frac{ie}{\hbar c} \partial\_\mu \chi(x) \right) \phi(x) $

So now your nice wave equation is a mess, and it varies from one place to another as a function of this $\partial\_\mu \chi(x)$ term. So here is the trick: you basically just add this annoying term into the overall EM potential field (which is OK because such additions do not change the gradients and therefore do not affect observable EM field vectors):

- ${A}\_\mu(x) \rightarrow {A}\_\mu(x) + \partial\_\mu \chi(x) $

And then you just subtract this whole thing back out from your messy equation, and this gives you something just slightly less messy:

- $\left(i \hbar \partial\_\mu - \frac{e}{c} {A}\_\mu\right)\phi $

So, this ends up being the same thing as the minimal coupling described earlier. Somehow, this whole process seems like a rather contrived way to end up with something that already made quite a bit of sense before hand. However, as noted earlier, the true payoff of such a procedure appears to come in addressing the weak and strong forces, which we leave for a future refinement of the model.

# Interim Summary

This is just a brief stop, to reiterate that we now have a full electrodynamic system with bidirectional interactions between a wave of charge and the electromagnetic force field. The wave equation remains at the core of both the charge wave and the electromagnetic field equations, but we did have to add in a few extra first-order spatial gradient computations here and there. All of this was necessary to get our electrodynamics working according to known physical laws. It may not be quite as elegant as our simplest system of a pure wave field for forces, and a simple scalar KG wave equation for our particle, but elegance cannot trump physical facts. Still, all the broad implications of those core wave equations (special relativity, Newtonian-like dynamics, quantum physics, etc) all hold for our more elaborated equations.

Perhaps the most surprising development here is that we had to break the symmetry between the two components of the complex state variable, and introduce a preferred direction of rotation, in order to avoid numerical instability. This numerical instability results when variables are coupled, and the rotation through the $\varphi_a$ and $\varphi_b$ variables produced by the interaction with the electromagnetic field is manifest as such a coupling. This break in symmetry and preferred direction of rotation bears a tantalizing resemblance to features of the weak force, suggesting a possible explanation for an otherwise very strange aspect of nature.

Our overall model at this point consists of a small handful of locally computable equations, which can be readily simulated on a computer. As these equations play out, they deterministically, locally, and automatically generate physics that should be largely consistent with what we know about the world. However, as we noted before, our equations are missing one critical piece, which is {\em spin}.

Interestingly, the introduction of spin creates a parity in the number of variables participating in the electromagnetic field equations (four) with those in the particle charge wave, which is currently two, but will now double to four. Overall, the elegance of having four variables each in two systems of interacting wave equations, which unfold in a four-dimensional space-time, seems suspiciously neat.

# Second Order Dirac Equation: Spin!

The final step in our long journey is to come to terms with the full glory of the electron. The standard model of physics has a set of parameters that are used to characterize the basic properties of the fundamental particles. One such property is the rest mass $m_0$, which we introduced into our particle-wave equation to make the waves slow down and move at variable speeds. Another such property is electrical charge, which we were able to extract from our wave equation once we used a complex-valued state variable, having two independent scalar values within it. Furthermore, we found that this charge could come with two different signs, positive or negative. This turns out to be convenient, because electrons also come in a positive form, called a positron. The positron has the same mass as the electron, but just an opposite charge.

The third basic property of the electron is known as its spin. It is known as a spin $\frac{1}{2}$ particle, along with all of the other fundamental particles know (e.g., quarks). Unfortunately, our wave equations so far do not support this spin property, and so we'll need to do a little bit more work. However, once we're done, we'll find that our equations capture all of the fundamental properties of the electron: we should have a 100% complete description of it! Actually there is one last thing, which is that the electron is a member of the {\em lepton} family, whereas the other fundamental particles are quarks, and they have other fundamental properties in addition to those carried by leptons. But, this is presumably because quarks live in some other set of state variables separate from the lepton state variables we're simulating here in our model. So, with that assumption, we might have captured everything about the electron.

So what exactly does it mean for an electron to have spin $\frac{1}{2}$? The quantum mechanical concept of spin is perhaps one of the most difficult to grasp. Sometimes people try to think of a little point particle spinning about like a top on its axis, but this doesn't actually fit the facts very well. In the end, the best strategy may be to just see what the equations we derive next actually do, and call that spin. Indeed, in the computer simulations, one can clearly see a spinning motion. This spin is very much like the first-order Schrödinger equation dynamics, where the two different elements of the complex variable rotate into each other. We also saw this kind of rotation earlier in the complex coupled KG equation, where the electromagnetic potential introduced a rotation among the complex variables. In the present case, we're going to have four different variables, and they will all rotate amongst themselves to produce this mysterious spin.

Incidentally, quantum physics holds that photons (which we think of as wave packets of the electromagnetic field that we've already characterized above) have a spin of 1. Furthermore, the charged complex KG wave equation is described as having a spin of 0. This latter case makes sense to me, in that the two components of the complex number do not rotate into each other, and thus they do not spin at all. However, the electromagnetic field case is a bit more confusing, because as we saw, the four components of this field do not interact with each other in the basic wave equations either! Therefore, it would seem that it should have a spin of 0 as well. Countering this are two considerations. First, the observable variables of the electric and magnetic fields $\vec{E}$ and $\vec{B}$, which are derived from these non-interacting electrical potentials, do rotate around each other as the wave propagates. Second, when these potentials interact with our charge wave, the do so in a way that ends up coupling (and rotating) the two independent scalar values in the complex number, and thus they impart some spin on our otherwise spinless particle.

Our first step is to introduce a new state variable $\psi$, to represent a field having four independent scalar values. Mathematically, this is defined as a vector of two complex numbers:

$$
\psi = \left( \begin{array}{c} \varphi\_{1a} + i \varphi\_{1b} \\
\varphi\_{2a} + i \varphi\_{2b} \end{array} \right)
$$

where the first complex number is denoted with a subscript $1$, and contains the two real-valued components $\varphi\_{1a}$ and $\varphi\_{1b}$, and the second has subscript $2$, and contains $\varphi\_{2a}$ and $\varphi\_{2b}$. So, the spin is going to amount to these four variables rotating amongst themselves.

How do we extend our basic complex-coupled KG equation to include this spin factor? Several authors in the literature have described a second-order version of the Dirac equation, which should look very familiar to you at this point, because it is essentially our current KG equation plus one additional spin term. One of the first references to such a thing comes from \incite{FeynmanGellMann58}, where they describe an equation that possesses all of the critical properties of the standard first-order Dirac equation, and note that it only requires four state variables instead of the eight required for the first-order equation. Indeed, Feynman states that he much prefers this form of the equation. This affection is presumably not widely shared, because there are relatively few other references to such an equation in the literature. Most of them come from a series of papers by Levere Hostler (e.g., Hostler, 1982, 1983, 1985).

The version of the equation described by Feynman & Gell-Mann (1958) is:

- $\left\[ \left(i {\nabla}\_\mu - {A}\_\mu\right)^2 + \vec{\sigma} \cdot \left(\vec{B} + i \vec{E} \right) \right\] \psi = m_0^2 \psi $

where $\vec{\sigma}$ are the standard Pauli matricies that we'll describe in a moment. Hostler (1985) describes a similar equation (which has the minus sign reversed in various places, but is otherwise the same):

- $\left\[ \left(-i \partial\_\mu - e {A}\_\mu\right)^2 + m_0^2 + e i \vec{\sigma} \cdot \left(\vec{E} + i \vec{B}\right) \right\] \psi = 0 $

It should be clear that the first squared term is just the complex KG equation coupled to the EM field. Therefore, we can write this equation in our current notation as:

- $\left\[\left(i \hbar \partial\_\mu - \frac{e}{c}{A}\_\mu \right)^2 + \frac{e}{c} \vec{\sigma} \cdot \left(\vec{B} + i \vec{E} \right) \right\] \psi = m_0^2 c^2 \psi $

Now for the Pauli matricies $\vec{\sigma}$. This is a vector of values $(\sigma_x, \sigma_y, \sigma_z)$ that enter into a dot product with the complex-valued vector composed of the magnetic and electric field values $\vec{B}$ and $\vec{E}$:

$$
\vec{\sigma} = \left( \left( \begin{array}{cc}0 & 1\\
1 & 0 \end{array} \right), \left( \begin{array}{cc}0 & -i \\
i & 0 \end{array} \right),  \left( \begin{array}{cc} 1 & 0 \\
0 & -1 \end{array} \right) \right)
$$

In the end, the net result of the dot product with an arbitrary vector $\vec{p}$ is:

$$
\vec{\sigma} \cdot \vec{p} = \left( \begin{array}{cc} p_z & p_x - i p_y \\
p_x + i p_y & -p_z \end{array} \right)
$$

So applied to our $\vec{B} + i\vec{E}$ vector, it is:

- $\vec{\sigma} \cdot \left(\vec{B} + i \vec{E} \right) = $

$$
\left( \begin{array}{cc} B_z + iE_z & B_x + iE_x - iB_y + E_y \\
B_x + iE_x + i B_y -E_y & -B_z - iE_z \end{array} \right) =
$$

$$
\left( \begin{array}{cc} B_z + iE_z & B_x + E_y + i(E_x - B_y) \\
B_x - E_y + i(E_x + B_y) & -B_z - iE_z \end{array} \right)
$$

So, now we're getting some sense of how this works: different components of the electromagnetic field exert different forces on the different components of the $\psi$ state, producing a rotational effect.

This entire result then is multiplied by the two complex numbers in the $\psi$ state:

$$
\left( \begin{array}{cc} B_z + iE_z & B_x + E_y + i(E_x - B_y) \\
B_x - E_y + i(E_x + B_y) & -B_z - iE_z \end{array} \right)
\times \left( \begin{array}{c} \varphi\_{1a} + i \varphi\_{1b} \\
\varphi\_{2a} + i \varphi\_{2b} \end{array} \right)
$$

Which produces this for the first complex number:

- $\varphi\_{1a} + i \varphi\_{1b} = (\varphi\_{1a} + i \varphi\_{1b})(B_z + iE_z) + (\varphi\_{2a} + i \varphi\_{2b})(B_x + E_y + i(E_x - B_y)) $

which decomposes into the two scalar variables as:

- $\varphi\_{1a} = \varphi\_{1a} B_z - \varphi\_{1b} E_z + \varphi\_{2a} (B_x + E_y) - \varphi\_{2b} (E_x - B_y) $
- $\varphi\_{1b} = \varphi\_{1b} B_z + \varphi\_{1a} E_z + \varphi\_{2b} (B_x + E_y) + \varphi\_{2a} (E_x - B_y) $

And for the second complex number:

- $\varphi\_{2a} + i \varphi\_{2b} = (\varphi\_{2a} + i \varphi\_{2b})(-B_z - iE_z) + (\varphi\_{1a} + i \varphi\_{1b})(B_x - E_y + i(E_x + B_y)) $

which decomposes into:

- $\varphi\_{2a} = -\varphi\_{2a} B_z + \varphi\_{2b} E_z + \varphi\_{1a} (B_x - E_y) - \varphi\_{1b} (E_x + B_y) $
- $\varphi\_{2b} = -\varphi\_{2b} B_z - \varphi\_{2a} E_z + \varphi\_{1b} (B_x - E_y) + \varphi\_{1a} (E_x + B_y) $

So, with the minus sign flip that took place in the main equation, and the fact that all of the rest of the equation operates on each complex component of $\psi$ separately, without any mixing across components, the final update equations for this second-order Dirac equation are just the basic complex KG equations plus these terms:

- $\ddot \varphi\_{1a} = \nabla^2 \varphi\_{1a} - m_0^2 \varphi\_{1a} + 2 e \left(A_0 \dot \varphi\_{1b} + \vec{A} \cdot \vec{\nabla} \varphi\_{1b} \right) + $
- $e^2 \varphi\_{1a} \left(A_0^2 - \vec{A}^2 \right) + e \left( \varphi\_{1a} B_z - \varphi\_{1b} E_z + \varphi\_{2a} (B_x + E_y) - \varphi\_{2b} (E_x - B_y) \right) $
- $\ddot \varphi\_{1b} = \nabla^2 \varphi\_{1b} - m_0^2 \varphi\_{1b} - 2 e \left(A_0 \dot \varphi\_{1a} + \vec{A} \cdot \vec{\nabla} \varphi\_{1a} \right) + $
- $e^2 \varphi\_{1b} \left(A_0^2 - \vec{A}^2 \right) + e \left( \varphi\_{1b} B_z + \varphi\_{1a} E_z + \varphi\_{2b} (B_x + E_y) + \varphi\_{2a} (E_x - B_y) \right) $
- $\ddot \varphi\_{2a} = \nabla^2 \varphi\_{2a} - m_0^2 \varphi\_{2a} + 2 e \left(A_0 \dot \varphi\_{2b} + \vec{A} \cdot \vec{\nabla} \varphi\_{2b} \right) + $
- $e^2 \varphi\_{2a} \left(A_0^2 - \vec{A}^2 \right) + e \left( -\varphi\_{2a} B_z + \varphi\_{2b} E_z + \varphi\_{1a} (B_x - E_y) - \varphi\_{1b} (E_x + B_y) \right) $
- $\ddot \varphi\_{2b} = \nabla^2 \varphi\_{2b} - m_0^2 \varphi\_{2b} - 2 e \varphi\_{2a} \left(A_0 \dot \varphi\_{2a} + \vec{A} \cdot \vec{\nabla} \varphi\_{2a} \right) + $
- $e^2 \varphi\_{2b} \left(A_0^2 - \vec{A}^2 \right) + e \left( -\varphi\_{2b} B_z - \varphi\_{2a} E_z + \varphi\_{1b} (B_x - E_y) + \varphi\_{1a} (E_x + B_y) \right) $

Again, it is fundamentally the wave equation, plus three additional terms that characterize the interaction with the electromagnetic field. Note that, as with the mixing across complex components $\varphi_a$ and $\varphi_b$ that occurred in the previous version of the coupled KG equations, the mixing or spin across $\phi_1$ and $\phi_2$ occurs via the electromagnetic field interaction. This time, the vector force fields are now required for the coupling, requiring that we compute them from the potentials, as described earlier (involving the $\vec{\nabla}$ first-order gradient and, for the first time, the $\vec{\nabla} \times$ function, which is very similar in its discrete form to the $\vec{\nabla}$ function).

% todo: run KG versions of the basic tests and see whether this is true!!!

Interestingly, although we need to continue the broken symmetry from the previous coupled-complex KG equation, where we use the current values of $\dot \varphi\_{1a}$ and $\dot \varphi\_{2a}$ to update the $\varphi\_{1b}$ and $\varphi\_{2b}$ variables, we apparently do not need to perform a similar symmetry breaking for the new couplings in this Dirac equation.

So, to answer the question of "what is spin?", we need only look at these equations. Spin, it seems, is this rotation of state values through the two complex variables in the $\psi$ state: $\phi_1$ and $\phi_2$. As is evident, this spinning occurs via interactions with the electromagnetic field vectors oriented along the three different spatial directions. The fact that, in our CA model we actually fix these directions according to the underlying cubic grid may seem strange and arbitrary. However, this does not mean that stuff can only spin along these fixed directions, anymore than it means that waves can only propagate in certain directions. By having different continuous values along these dimensions, any "direction" of spin relative to the underlying grid can occur.

Although somewhat complex, these equations should describe the entirety of the complexity of the electron's interaction with the electromagnetic field, which is to say, with other electrons and positive electric charges in the nucleus. Therefore, as we know, a huge proportion of the known complexity of the universe stems from the consequences of these basic equations. So, perhaps they do not look so complex in comparison.

% todo: introduce coupled complex KG (CCKG) equation nomenclature % todo: also introduce covariant derivative term

One final thing to note is that the charge and current density equations from the previous version of the coupled complex KG equation still hold for this Dirac version, because these additional terms to not enter into the covariant derivative, and are therefore canceled out in the subtraction, just like the mass term. The actual numerical calculation changes only to accommodate the $\psi$ state value instead of the single complex $\phi$ state. The charge and current equations are:

- $\rho = \frac{\hbar e}{m_0 c^2} \left((\varphi\_{1b} \dot \varphi\_{1a} - \varphi\_{1a} \dot \varphi\_{1b}) + (\varphi\_{2b} \dot \varphi\_{2a} - \varphi\_{2a} \dot \varphi\_{2b})\right) - $
- $\frac{e^2}{m_0 c^2} A_0 (\varphi\_{1a}^2 + \varphi\_{1b}^2 + \varphi\_{2a}^2 + \varphi\_{2b}^2) $
- $\vec{J} = \frac{\hbar e}{m_0 c^2} \left((\varphi\_{1a} \vec{\nabla} \varphi\_{1b} - \varphi\_{1b} \vec{\nabla} \varphi\_{1a}) + (\varphi\_{2a} \vec{\nabla} \varphi\_{2b} - \varphi\_{2b} \vec{\nabla} \varphi\_{2a})\right) -$
- $\frac{e^2}{m_0 c^2} \vec{A} (\varphi\_{1a}^2 + \varphi\_{1b}^2 + \varphi\_{2a}^2 + \varphi\_{2b}^2) $


