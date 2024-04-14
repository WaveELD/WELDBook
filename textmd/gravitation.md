# Gravitation

The problem of reconciling quantum mechanics and gravitation as described by Einstein's general theory of relativity is currently unsolved, and introduces many obstacles for the standard QM interpretations, which do not even admit to a well-specified source of gravitational mass / energy outside of the moments of wave function collapse.

The Bohmian perspective in general provides a potentially fruitful avenue toward this reconciliation, because matter particles at least have a definite physical location at all times.  However, given that these are point particles, they represent a gravitational singularity, which must be resolved, in the same way that the EM singularity must be resolved for electric charges.  The WELD cellular automaton (CA) framework provides a natural "ultraviolet" cutoff point for any such singularities, in the form of the fixed underlying grid spacing (i.e., the _matrix_).  

However, the size of this grid spacing is not directly constrained by the basic electrodynamic physics: we can "renormalize" the relevant constants to accommodate any such grid scale, so we need some additional form of physical data to provide relevant constraints.  As the grid size gets smaller, the strength of gravitational effects increase, putting greater pressure on the need to incorporate gravitation as a central element of the framework.

The most natural way to incorporate a general relativity-like gravitational dynamic into the CA model is to have coupling constants between each cell that reflect the local curvature of space in each direction.  As curvature increases, the effective distance between cells increases, reducing the strength of the wave transmission across them.  As with the wave dynamics operating within the discrete CA framework, this would obscure the underlying flat grid space, except that, in the absence of any mass / energy generating these curvatures, "empty" space would be flat.  Perhaps not coincidently, the universe is known to be flat.  Furthermore, from the WELD CA perspective, time and space are both infinite, which is just slightly less implausible than having some kind of edge beyond which nothing exists. 

This CA gravitational model avoids any kind of mathematical singularity in the context of black holes: there is just more energy and particles packed into a smaller space, which, due to Lorentz dynamics oscillate at slower and slower rates, and contract to smaller and smaller sizes, and drive more curvature, such that electromagnetic fields do not propagate out of the central region.  Indeed, the ability to simulate such black hole dynamics represents a critical stress test for the overall framework.

Before continuing to develop this gravitational model, we can consider whether there are available data to fix the approximate grid size.

## Constraints from Cosmology

The natural cosmology for a flat, infinite space populated by ever-growing non-singular black holes is to think of the big bang as resulting from the accumulation of matter / energy into a single huge black hole that grows up to a hypothesized point of a maximal density, at which point it explodes, spewing forth a new clean slate of matter to begin the process all over again.  This is an appealing [cyclic model](https://en.wikipedia.org/wiki/Cyclic_model) (wikipedia link) of cosmology, of which many forms have been developed.

If we can compute how dense matter must have been at the moment of the big bang, this might fix a grid scale capable of just representing this density.

The most widely accepted (though still widely regarded as _ad hoc_) model of the big bang involves a period of _inflation_ where a presumed singularity expands "magically" (no known physical force or process is a plausible candidate) for a very brief moment (from $10^{-36}$ sec to $10^{-32}$ sec after the big bang) at an exponential rate, such that the universe at the end of inflation is approximately the size of a grain of sand: $0.88 x 10^-3$, according to this [physics stackexchange](https://physics.stackexchange.com/questions/32917/size-of-universe-after-inflation).

The physical consequence of such a process (i.e., the entire reason for its hypothesized existence) is to create the flat, relatively homogeneous, isotropic universe that we observe today.  Without inflation, the huge energy density of the big bang would create massive amounts of "quantum foam" during expansion, which would make the universe very inhomogeneous and highly curved.

In our alternative cosmological framework, this grain of sand, containing all of the mass / energy of the universe, would represent the maximum energy / particle density that a black hole could support.  Because the flatness of space is a given in this framework, we would only need to explain why this initial black hole state would result in a relatively homogeneous and isotropic distribution of mass and energy.  Perhaps because it spent a long time bouncing around in this grain of sand prior to blowing up?

It is highly uncertain (to me at least) what physics would look like within this primordial black hole.  Is it just pure energy or do the fermion particles remain in some fashion?  Presumably, due to the high energies present, we would need the "full" standard model including quarks etc to represent this state.  I guess it might be some kind of [quark-gluon plasma](https://en.wikipedia.org/wiki/Quark%E2%80%93gluon_plasma)?

## Spin Coupling to Gravity

There is a particularly relevant line of work from Nikodem Popławski, building on earlier work from Kopczyński (1972) in the Einstein-Cartan-Kibble-Sciama (ECKS) theory of gravity (Hehl et al, 1976).  This form of gravity adds a coupling of the spin component of a fermion particle to the gravitational metric tensor, adding a _torsion_ component.  The net effect of this torsion is a significant repulsive force when the density of fermions goes up (Popalawski 2010; 2012; 2016). This repulsive force would prevent a black hole from fully collapsing into a singularity, and instead it would "bounce" or oscillate as the mass / energy  attractive gravitational force interacts with this repulsive force. 

Popalawski (2012) gives the following estimates for the big bang parameters:

* critical temperature $T_cr = .75 m_p$ (what is m_p?)

* critical radius $≈ 5.9 × 10^{−4} m$ (from which the density could be computed)

* momentum? frequency? associated with the critical temperature: $v(T_cr) ≈ 8.9 × 10^{34}$  (total energy?)

Popalawski (2010) defines the Cartan radius of an electron to be on the order of $10^{-27} m$, which sets a minimum spatial scale for such a particle. The density of electrons all packed together at this radius would be $ρ = m_e / r^3 = 10^{51} {kg} m^{−3}$.

## Pauli Exclusion in Black Holes

The Pauli exclusion principle, i.e., the spin statistics theorem, says that two fermions cannot occupy the same quantum state, and this is understood to prevent a neutron star from further collapsing upon itself.  Why doesn't the same principle apply within a black hole?  This is not well understood apparently, at least according to this [stackexchgange](https://physics.stackexchange.com/questions/93988/does-black-hole-formation-contradict-the-pauli-exclusion-principle) discussion, in large part because quantum mechanics and gravity have not been reconciled, and even the precise ways of working with singularities within black holes are unresolved (Geroch, 1967).

In any case, it is unclear if the exclusion principle itself would provide the kind of critical density scaling parameters that we would like.  Perhaps the above spin-torsion framework may provide a better answer?  And what is the relationship between the gravitational spin dynamic and the exclusion principle anyway?  Perhaps there is some deep connection?

## Planck scale

Another approach is to consider the Planck scale, where all the units involved in the gravitational equations take on a value of 1, which sets the Planck length on the order of $10^{-35} m$.  See [Physics Forums](https://www.physicsforums.com/insights/hand-wavy-discussion-planck-length/) and [John Baez Lengths](https://math.ucr.edu/home/baez/lengths.html) more info.  At this length scale, the gravitational force immediately surrounding an electron is as strong as its EM force.  The smallest length that has been empirically measured, according to above link, is about $10^{-22} m$, which is well below the Compton wavelength of an electron (order $10^{-13}$).


## The Extreme Coincidence of Flat Space

Nothing in the math of general relativity requires that the overall spacetime metric of the universe be flat, and yet it is.  In the standard inflationary big bang model of cosmology, a very precise set of parameters is required to end up with a flat result, making the entire construct of inflation even more implausible and ad hoc.  The idea that flat spacetime just a coincidental consequence of these specific initial conditions seems to be missing a huge opportunity for understanding that the universe seems to telling us very clearly: **spacetime is flat because space is fundamental**.  Space is not just some arbitrary mathematical construct, but rather it is the substrate upon which physics operates, as captured in the cellular automaton (CA) framework.  And flat spacetime is the natural consequence of the simplest cubic tiling of 3D space.

Because we populate our CA space with waves, this underlying cubic structure disappears, and physics behaves in an invariant manner across reference frames, consistent with relativity.  But the fact that it is so implausibly flat seems to be crying out for a deeper explanation.  Also, the need for renormalization and to avoid all manner of singularities and infinities that arise in the limit of infintessimal, continuous space, strongly suggests that there is an "ultraviolet" cutoff: space is not continuous, but discrete, with a minimum underlying grid size.


