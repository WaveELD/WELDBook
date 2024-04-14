TODO: this page is out of date -- needs integration.

This page provides an accounting of all the major phenomenology of physics that strongly constrains theorizing, along with how different frameworks account for these phenomena. It is mostly a device for thinking through these issues and is not really intended to be comprehensible to people not otherwise familiar with the phenomena and theories.

# Philosophical Foundations

First, the bedrock philosophical principles governing the approach:

- Despite the primacy and limitations of our inevitably subjective windows onto reality, I believe there is an objective reality that exists outside of my mind.

<!-- -->

- As such, this reality must somehow *function [autonomously](autonomous "wikilink")* -- it just happens, even when nobody is looking. The notion that the human mind plays any kind of special role in physics seems strongly inconsistent with all available evidence that our minds evolved very recently in astronomical time.

<!-- -->

- Autonomous functioning systems are *mechanistic* -- they have certain rules or laws, operating on some kind of *something*, and, given a set of initial conditions of the universe, proceed to generate the unfolding of phenomena that we observe from our narrow subjective human windows.

<!-- -->

- We do not know if we can understand these laws, but we do have a *standard model* that, despite its many limitations, provides a very accurate means of predicting the outcomes of experiments. One of the most important limitations of this standard model is that it does not provide an autonomous, mechanistic understanding of physics. It allows us, under very limited situations, to compute predicted outcomes, but many core hurdles prevent us from running a numerical simulation of the model autonomously evolving over time to describe even the most essential and basic phenomena such as the hydrogen atom absorbing and emitting electromagnetic radiation -- again we can compute predicted outcomes to high accuracy, but we can't even in principle "run" such an atom as a complete system evolving autonomously over time. The question then is: how does *nature* run? Can we ever understand the answer to such a question? Most practicing physicists have long eschewed such a question in favor of the "shut up and calculate" approach -- the barriers to deriving a "mechanistic" framework of quantum physics are so seemingly daunting that most have long-since given up such a futile adventure. But as a non-practicing non-physicist, I have the luxury of such futile pursuits!

<!-- -->

- The central gambit here is that, perhaps, by thinking through what it would take for nature to "run" autonomously, we can develop a more satisfying theoretical framework overall. Instead of starting from more abstract "elegant" principles like symmetry, we take a more gritty, pragmatic perspective: what would it take to make an autonomous system that does everything nature does? There are a lot of amazing things going on here -- lots of different tradeoffs and compromises -- maybe by understanding those from a "design" perspective, we can figure out why it is the way it is? Maybe there are a really small, even singular, set of mechanisms that are the simplest set of things that make "interesting" stuff happen? e.g., pure waves do a lot of great things, but they also just fall apart -- need to add in some particle rectification -- how do you get that to play well with the waves, etc?

<!-- -->

- Of course, the most important overriding consideration in this pursuit is: the *truth* -- ultimately we need a mechanistic model that generates all of the known phenomenology of physics, and this wiki page is an attempt to keep an accounting of that scope of phenomenology. As every student of physics knows, however, there is great utility in simpler approximations and models that *intentionally* omit certain complexities in the service of rendering core principles clearer and easier to compute: the fictitious frictionless plane, etc. And the pursuit of ideas in physics is riddled with seemingly great ideas that just don't "work" for one reason or another. Sometimes, just a few tweaks can turn those into the great ideas that *do* work.. In the course of developing this approach, for example, the pure-wave WELD idea seemed like it could "go all the way", but after further investigations and reflections, major limitations are apparent.. Thus, the path is not straight, and it is *essential* to be clearly mindful of the limitations of any given framework or model -- this can be challenging in early stages when such limitations are not yet obvious, and the potential seems so compelling. But the long arc of physics always bends toward the truth, eventually..

# Space-time

## Core phenomena

- Physics appears to operate within 3 spatial dimensions, evolving over time.
- With the notable exception of non-locality effects in QM, many phenomena are compatible with strictly local interactions within spacetime -- the light-speed cone of causality etc.
- Cosmologically, space seems remarkably, suspiciously flat.
- Philosophically, it seems overall more elegant to imagine that space is infinite in extent and time -- this avoids the inevitable conundrums of "edges" in spacetime -- something outside the bubble of the big-bang or whatever.

## Implications

- From the mechanistic, autonomous perspective, the cellular automaton framework (CA) fits exceptionally well with these basic facts of spacetime. This is a foundational principle of the WELD approach. Space is primary, and physical rules are defined as update equations operating on cubic cells of primary *stuff*. The speed of light emerges naturally from this framework. It can easily accommodate all of classical EM -- we have a nice implementation of Maxwell's equations within this framework.

<!-- -->

- But QM nonlocality flies in the face of this framework. Now that we have to take this seriously, we need to see if all the "pros" of the CA framework can be somehow augmented with whatever it takes to accommodate nonlocality, or whether it needs to be discarded entirely as a nice idea that simply doesn't "work".

# Waves

## Core phenomena

- EM -- per above.
- Dirac wave equation -- relativistic generalization of Schroedinger equation -- can be implemented nicely within CA framework (in its second order form).
- two-slit interference, etc -- all good..

## Implications

- Love the waves! can't get enough of them!

<!-- -->

- Major problem with current impl: leaky waves -- waves are spreading out all over the place -- electron wave doesn't remain contained within atomic system. What if this is due to 26 neighbor model that nicely deals with grid aliasing artifacts, but maybe we really need to separately propagate along each of the canonical axes, like what happens with the A, B vector fields in EM? spread is no problem in 1d Schrodinger models really -- seems like nobody really worries about this as far as I can tell -- always using 1d and generalizing from there? 3d = just sum of 1d cases?

<!-- -->

- Bialynicki-Birula (1993) and David Meyer (1996?) models: uniqueness of conservative (unitary) local transfer functions, require bidirectional flow -- need to investigate those, esp BB.

<!-- -->

- Another approach: lattice particles with wave-functions on the links can potentially regularize wave dynamics -- digitizes wave functions at every step..

# Particles

## Core phenomena

- Strictly quantized, conserved charge
- Conserved fermion number
- Scattering, scattering, scattering! how do waves ever scatter!?
- Photoelectric effect? maybe more about atoms than EM? maybe not though? hmm. Semiclassical literature etc can get pretty far -- what are the remaining phenomena that we need to deal with? photon-based entanglement maybe the most strong?
- Particles transform into other particles! what are the rules that govern creation and destruction of particles?? this basic fact greatly complicates any particle model -- would have been much simpler to think of particles as hard little permanent things -- but they are only partially that. other times they are rather fluid..
- Furthermore, many particles are strictly temporary and unstable -- what makes them unstable?
- Virtual particles -- short-lived but "real" -- have measurable effects.. what is the deal!?

## Implications

- all really challenge pure wave-based approach, *except* the fluidity of particles and and virtual particles -- but emergent particles within a pure wave framework doesn't seem likely to handle all the strong particle phenomena.
- as we know from QM, once you fully acknowledge the dual wave-particle reality, all the conundrums emerge. the pure-wave dodge isn't going to work. we need to confront this head-on.
- classic copenhagen / Born rule approach is non-starter as mechanistic theory: doesn't define when collapse happens, depends on vaugely-defined "measurement" events, etc.
- Bohm is very appealing: particles always somewhere, have well-defined trajectories, no collapse. all the nonlocality is in the wave function -- particles themselves are fully in 3D spacetime.
  - doesn't have a good relativistic formulation? actually it does -- H. Nikolic has shown this.
  - doesn't deal with fluidity of particles -- also work by Nikolic attempts to merge QFT particle creation / destruction with Bohmian world view.
- Quantum Field approach (QED): fourier space, particles are modes of vibration -- naturally non-local, deals with particle transformations, virtual particles..

# Zero point energy and coherent background field effects

- There is a non-zero background energy level in a 2nd quantized system -- this plays a critical role in the stochastic electrodynamics (SED) and stochastic optics models (Marshall & Santos, 1988; Marshall & Santos, 1997; de la Pena & Cetto, 1996) -- the ZPF = Zero Point Field.

<!-- -->

- In the oil drop simulations of QM, the wave field emerges from a coordinated shaking of the fluid.

<!-- -->

- I think the ZPF / ZPE seems to emerge because of the synchronization of all the points in a lattice?? if we have a big lattice system, all phenomena may emerge as disturbances on top of a coordinated synchronized vibrating field. Disturbances themselves can propagate at the "speed of light" in such a system, but perhaps some nonlocal things could happen in terms of coordinated changes across the entire field???

## Quantum Harmonic Oscillator (QHO) and second quantization

Trying to make sense of the foundations of QFT -- key pages: <https://en.wikipedia.org/wiki/Quantum_harmonic_oscillator> <https://en.wikipedia.org/wiki/Phonon> <https://en.wikipedia.org/wiki/Normal_mode> <https://en.wikipedia.org/wiki/Zero-point_energy>

- The basic QHO and phonon theory is derived from classical wave equations, where the acceleration is proportional to distances from neighbors, as derived here: <https://grey.colorado.edu/WELD/index.php/WELDBook/Waves>

<!-- -->

- The "mass" and "spring constant" coupling relationship of the particles in the lattice model determine the speed of propagation, equivalent to the speed-of-light squared (c^2).

<!-- -->

- As near as I can tell, second quantization of this lattice field amounts to the following moves:

<!-- -->

- - Representing everything in terms of the normal modes of oscillation. The normal modes are an orthogonal basis set of sine waves across the entire state, in multiples of the fundamental frequency. In other words, Fourier space.
  - This also clarifies the situation a bit: <https://physics.stackexchange.com/questions/122570/which-is-more-fundamental-fields-or-particles> -- the original state-based formulation in terms of wave functions for particles is a problem because particles are indistinquishable from each other and thus it has 2x the amount of info and needs to subtract that out -- representing in terms of Fourier space doesn't have that problem.
  - It seems implicit that the states one is considering are all "contextualized" or "conditioned" on a particular situation -- they are not true [autonomous](autonomous "wikilink") states -- in other words, they are like the violin string -- about a particular constrained object like an electron in an atom -- they cannot apply more generally because then the particles extend across the entire universe in the Fourier representation.
    - Indeed, <https://physics.stackexchange.com/questions/248754/what-do-the-wave-functions-associated-to-the-fock-states-of-each-mode-of-a-bound> states that "Each fock state has an associated wave function" -- i.e., the QFT bookkeeping is not the full picture -- there is an additional wave function associated with each such state! This might be relevant: <http://iopscience.iop.org/article/10.1088/1751-8121/aa70ba/meta>
  - Critically, *there is no fundamental quantization* to the field. In the continuous Fourier space, there isn't any natural cutoff to the frequencies, or preferred fundamental frequency. This is truly just a bookkeeping device for tracking whatever frequencies or energies might be relevant for a given "contextual" situation -- you apply the QFT to describing a *specific* state that does have relevant quantization dynamics due to atomic confinement etc..
  - In the discrete, lattice-like QHO model, there *is* a cutoff, highest frequency, and Planck's constant could possibly be related to the distance between lattice sites here. Need to look at <https://en.wikipedia.org/wiki/Natural_units> -- e.g., the Planck scale could be defined much higher if we ignore G, which is what drives things so tiny in space and time, and so huge in mass scale. E = hv proportionality doesn't imply any specific limit on frequency or wavelength.. Paper about discretization cutoff with various relevant discussion: <https://arxiv.org/abs/1210.1847>
  - There is still *some* kind of quantization because particles are represented as integer-valued multiples of these normal modes? The amplitudes are not continuous, but quantized. This is perhaps the key discrepancy from the classical system?
  - Due to the Fourier representation of the system, a particle corresponds to one of these discretized modes being created across the entire universe -- i.e., there is no spatial localization. what!?
  - The zero point energy corresponds to a non-zero fluctuation in this field -- various ways of understanding this: for real particles, they have to have a wave function, and a wave function always implies some kind of oscillation (e.g., rotation among the real / complex components) -- this oscillation persists even when there is no overt motion of the particle (i.e., the momentum factor is zero -- momentum = curvature of wave, so this would be a perfectly "flat" wave..)

<!-- -->

- Bottom line: as usual, the question is what is the physics and what is the math here? seems like quantization and resonance are key -- is this just discretization?
- do neighbors really interact, or not? the fourier expansion seems to get rid of them..
- how is a localized particle ever represented!? phase interference effects of course.

# Nonlocality of entanglement

So many attempts to explain this phenomenon really fail to confront the nonlocality head-on, and invoke things like the no-communication theorem or some kind of weird predeterminism or even the many-worlds view, all of which fail to truly confront the nonlocal nature of the phenomenon. For example, this article by a nobel-prize winning physicist: <https://www.quantamagazine.org/entanglement-made-simple-20160428/> denies the mystery of nonlocality by appealing to a hidden variable account, without even so much as realizing it:

"Nor is it paradoxical to find that distant events are correlated. After all, if I put each member of a pair of gloves in boxes, and mail them to opposite sides of the earth, I should not be surprised that by looking inside one box I can determine the handedness of the glove in the other. Similarly, in all known cases the correlations between an EPR pair must be imprinted when its members are close together, though of course they can survive subsequent separation, as though they had memories. Again, the peculiarity of EPR is not correlation as such, but its possible embodiment in complementary forms."

That is exactly a hidden variable account: entanglement creates complementary states in two particles (like the two hands of a pair of gloves), and those two gloves fly off in different directions, to be measured later -- absolutely reasonable and sensible that they should have opposite handedness. Unfortunately, this is completely wrong from a QM perspective as several commenters point out, and it completely elides the entire absurdity of the nonlocality!

The logic really isn't that complicated: the wave function for an entangled system fundamentally expresses the necessary unitary nature of the conservation of some kind of property (spin, polarization, etc). If you start out with X amount of spin (e.g., 0), then whatever spin is measured at A must be compensated for by an offsetting spin at B so that the net spin is still 0. This, together with the critical idea that the state is truly indeterminate until measured, necessitates that the measurement process on one part of the wavefunction must have immediate, nonlocal implications for the measurement on the other part of the wavefunction. If both end up measuring "spin up" then there is a clear violation of the conservation of spin. There really is no way to have this happen "physically" without *whatever* is happening during measurement at location A somehow be "communicated" back to location B to properly influence the measurement outcome there. Whether "Alice" can send a message to "Bob" using this mysterious nonlocal communication channel (the no-communication theorem) is quite beside the point: *something* is truly nonlocal about this process!

One major problem with this conundrum is that there isn't a "physical" model for *any* of the processes involved. We don't even know if the wavefunction itself is "real", and we certainly don't know what a "measurement" is. So that makes it a bit strange to start talking about the physical nature of the nonlocal communication process when a wavefunction collapses during measurement. It is all very abstract math, and at that level, it makes for nice clean calculations

The main "physical" attempt to understand measurement is through decoherence: as a quantum state interacts with the measurement apparatus, the wavefunction does not actually collapse, it is just so strongly "hammered" by the measurement process that only one of the relevant eigenstates survives. But I haven't seen any explanations of how this kind of decoherence process would ensure that the other half of the wavefunction should always collapse the other way. For example, why couldn't a *local* conservation of spin operate within each half of the overall wavefunction, when taking into account the full state of the measurement system together with the incoming thing being measured (photon, electron, or whatever)?

This entanglement / nonlocality really cuts to the heart of core issues in QM. One major question is whether the wavefunction is something "physical" or just "epistemological" -- something that describes our state of knowledge, but not something that actually "exists" in nature. If it is purely epistemological, then somehow the nonlocality problem seems to evaporate: the collapse of a non-physical wavefunction presumably cannot itself be a physical process, so, somehow, thinking about a physical signal going across space doesn't make any sense either. But in this case, we are still left with the fundamental mystery: changing the measurement settings at A *somehow* really does affect outcomes measured at B. Calling the wavefunction epistemological seems to just avoid any attempt to answer this problem. Indeed, this is really the problem with the entire Copenhagen interpretation: it avoids all the hard questions and essentially amounts to the classic "shut up and calculate" approach -- just stick to the abstract math and don't worry about the physics.

The deBroglie-Bohm framework ascribes physical reality to the wavefunction, and explicitly makes it nonlocal to account for the relevant data. This seems like the only framework that isn't just ducking the problem using one sleight-of-hand or another.

Some other relevant points:

- Are we putting too much "reality" into the outcomes of measurements? There is this assumption that measurement extracts some "true" property of a thing. But measurement is known to be "contextual", and really it makes more sense to think of it as "creating its own reality" -- e.g., the above figure of polarization just rotating light around -- intermediate filtering can "rescue" light that would otherwise have been blocked. There is evidence that nonlocality and contextuality are manifestations of the same thing: <https://phys.org/news/2016-03-features-quantum-mechanics.html> -- <https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.116.090401> . The problem is that contextuality makes perfect sense, while nonlocality makes no sense, but it doesn't seem like we can just always have contextuality and somehow get rid of nonlocality? Anyway, understanding this more clearly seems like an important direction.

<!-- -->

- if wavefunction collapse is an illusion, and measurement is always "contextual", then what are the implications for the conservation logic behind nonlocal entanglement? There isn't any reality to the thing being measured in the first place -- it is just a "construction". So why does measurement in one place have to have any implication for measurement elsewhere? Except that apparently it does.. This seems to get back to the contextuality vs. nonlocality tradeoff issue -- where contextuality is absent, nonlocality holds..

<!-- -->

- Standard Hilbert-space formulations of QM reinforce the notion that the choice of a basis set is essentially arbitrary. But the Schrodinger equation, and more strongly the Dirac equation, and QED and all the field theoretic frameworks of the standard model, are manifestly *not* formulated about arbitrary probability distributions floating around. They are about a specific Hamiltonian describing particles with specific masses interacting with EM fields in specific ways, etc. The frequency (spatial gradient) of the wave function describes the momentum of the particle, while second-order temporal derivative describes its energy. There is manifestly here a very specific ontology and a strongly preferred basis. Mathematically perhaps things can be rotated and transformed in various ways, but it really seems like there are strongly relevant properties being represented here, that constitute the reality of something like an electron. And these are represented by wave functions. The whole apparatus of the standard model is just one big wave function after another. So it really seems like the wave function is what is real, if anything is. This is the initial premise of the WELD approach.

<!-- -->

- If the Dirac wave function is the only "true" reality of the electron, and it never collapses, then all measurement is definitely a "contextual" fiction -- the wave always remains a distributed thing across space and time. But how then do we explain that if we find something in one place, we don't also find it somewhere else? The wavefunction has to get squeezed into a small space -- in general in our WELD models this kind of squeezing of the wavefunction has been difficult. This is the mystery of the Born rule collapse function: it magically digitizes these crazy waves. Again we circle back to these fundamental mysteries. The pure wave picture seems to be incompatible with this Born magic, unless we can find some better ways of keeping the waves localized. Second quantization seems like the key thing missing from the simple classical-esque pure wave framework. Need to learn more about that.

<!-- -->

- It is worth pointing out that the wave fields are fully conservative -- they are indeed derived on the basis of conserving energy, and total charge. Thus, we don't explicitly need nonlocality per se to obtain conservation -- pure wave propagation without ever collapsing would automatically conserve everything properly. It is really only when collapse itself is invoked that nonlocal logic arises: if we don't reify the existence of "spin up" as a precise discrete thing at the moment of collapse, then we just have ongoing continuous wave propagation, with some kind of macroscopic illusion of having learned something "definitive" about the state of these waves.

<!-- -->

- There is something deep and mysterious about the positive and negative charge states of the complex KG and Dirac equations, which seems somehow related to the need for bidirectional flow in simpler CA models from Bialynicki-Birula (1993) and David Meyer (1996?). Is there something here that could explain nonlocality: these two channels are somehow coupled and paired, and when something affects one, it immediately affects the other!? Relatedly, why do we need spin? complex KG seems fine. but coupling with EM requires spin. Which then does introduce a coupling between the otherwise separate fields of complex KG. maybe this coupling is essential to allow for nonlocal conservative processes of some sort?

<!-- -->

- todo: examine this more carefully: <https://web.archive.org/web/20151117174141/http://www.mth.kcl.ac.uk/~streater/EPR.html> -- makes strong claims of locality but not sure what the error might be..

<!-- -->

- <http://www.mat.univie.ac.at/~neum/physfaq/therm/thermalMain.html>: "Therefore in the EPR sense, sources and beams are much more real than particles. The former, not the latter, are the real players in solid foundations. That's why an inappropriate focus on the particle aspect of quantum mechanics creates the appearance of mystery. It is a historical accident that one continues to use the name particle in the many microscopic situations where it is grossly inappropriate if one thinks of it with the classical meaning of a tiny bullet moving through space. Restrict the use of the particle concept to where it is appropriate, or don't think of particles as *objects* - in both cases all mystery is gone, and the foundations become fully rational."

# Lattice Field Model

The lattice field model (https://en.wikipedia.org/wiki/Lattice_field_theory) of QED / QCD has many potentially appealing aspects:

- QED as typically formulated in Fock space etc is founded on a *particle-identity* framework -- it is keeping track (indexed) by an infinite list of particles -- these particles are either created or destroyed by the appropriate operators.

<!-- -->

- Instead, in the lattice model, you just have potential ("virtual") particles at each location in the lattice, and these are either on or off. This is a powerful inversion of the traditional logic:
  - The fundamental notion of QM, that something doesn't exist until it is observed, is taken to a kind of extreme: particles do not exist as identifiable, stable entities -- there is just a conservation of relevant factors (charge, energy, momentum, etc) that governs the activation of these "virtual" particles at different locations.
  - In effect, each discretized location is space is continuously performing a measurement, deciding whether a virtual particle should be actualized momentarily at that location -- instead of quantum measurement being a rare, ill-defined process, it is a constant, continuously occurring process. Critically, unlike wave-function collapse versions of this general idea (https://en.wikipedia.org/wiki/Objective_collapse_theory), the measurement process here is just the actualization of a particle -- the wave function continues to propagate as usual, and decoherence (https://en.wikipedia.org/wiki/Quantum_decoherence) can explain the classical measurement issues.
  - This potentially puts "virtual" and "real" particles on the same footing -- presumably this is a known feature of lattice methods -- virtual particles in QED / QFT in general have had a somewhat mysterious ontological status -- clearly playing an essential role in the math, but often neglected in various philosophical / interpretational discussions.
  - Also overall consistent with the notion of particles as a digital rectification of an underlying analog system -- each lattice location computes such a rectification.

<!-- -->

- Lattice model is fundamentally like a cellular automaton and thus consistent with overall approach.

<!-- -->

- Major issues: nonlocality as ever -- does conservation require some kind of nonlocal tracking of particles? when a particle is realized in one location, how do you ensure that it doesn't also show up somewhere else?? tracking particles by identity like this is fundamentally at odds with all the advantages listed above -- particles shouldn't have an identity as such -- the wave function should not be about an individual particle -- it should be about all particles of a given type.. but can this work in practice? and does it just reduce to the same kind of sloppy fluid dynamics as the pure wave approach?
  - key idea: yes, nonlocality is fundamentally required for particle discretization in the context of particle number conservation (baryon number). otherwise, you end up with goofy local handoff of particle bits from one lattice cell to another -- logic is very hacky. Nikolic shows that Bohm model in relativistic case requires faster-than-speed-of-light motion -- this is not compatible with some kind of local particle passing algorithm. So the crux of the problem is how to heuristically discretize the continuous wave field in a way that does not actually require tracking particles as separate entities (which is implausible due to fluidity of particle creation and destruction etc -- fundamental constraint -- number is only kinda conserved and all particles are identical so you can't get into business of enumerating them EVER -- hard constraint).
  - one idea: integrate over a given spatial extent at every step and put a particle at the local max if probability density is above some threshold. kinda crazy but might just work.. how big is the area?? interesting..
  - having many update cycles of the wave equation within each particle update event or something like that would be far preferable to true nonlocality -- a very fast clock can look like nonlocality, and again the barrier of nonlocality is so high in terms of the central feature of [autonomous](autonomous "wikilink") models (how do you do any computation that requires infinite sums!?) -- we try to avoid it at all costs..

## Links

- <http://www.physik.uni-bielefeld.de/~laine/lattice/cover.html> -- lecture notes on lattice models (hand written)
- <http://www.thphys.uni-heidelberg.de/~sexty/lattice/> -- class on lattice -- also hand-written notes
- Smit book: <https://books.google.com/books?id=KIHHW9NtbuAC&printsec=frontcover#v=onepage&q&f=false>
- <http://www.qubit.it/research/publications/1601.04842.pdf> -- recent CA models paper
- <https://arxiv.org/abs/quant-ph/0603164> -- stochastic schrodinger -- why are people still using the schrodinger equation!? crazy.</text>
