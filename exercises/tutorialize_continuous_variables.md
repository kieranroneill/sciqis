# Tutorialize continuous variables

_Practice_

In this exercise, your goal is to prepare a Jupyter notebook that could introduce fellow students to the basics of [continuous variables](https://en.wikipedia.org/wiki/Continuous-variable_quantum_information) (CV) with a focus on some simple states of the [quantum harmonic oscillator](https://en.wikipedia.org/wiki/Quantum_harmonic_oscillator). The notebook should contain a mixture of explanatory text, equations, code, and visualisations (which could be interactive or animated, if you want). Here, the focus should mainly be on the presentation and the physics, not too much on code quality.

Some of you are almost experts on CV quantum optics, some of you may have only briefly met the QHO in introductory quantum mechanics. You also have very different coding experience. As such, the outcomes of this exercise will also be very different, which is perfectly fine. You should just make an effort to make as good a tutorial notebook as possible and cover as much or little theory as you can. 

1. Study the references below or find your own.
2. Start playing around with ways to visualise or otherwise present some basic and/or advanced concepts from continuous variables (see suggestions below if you don't know where to start).
3. Gradually combine your findings into a nicely formatted single notebook. Include Markdown cells with section headers, explanatory text and formulas. Try to make a coherent narrative throughout. Don't worry too much about getting everything perfectly right – think of this as a first draft you might improve upon later.
4. At the end of the day, submit your notebook as a pull request on the sciqis Github repository (instructions below). On Monday, you will give feedback to each other.

### References

In quantum optics, an important class of quantum states are those with Gaussian wavefunctions over the x-quadrature (often also called position or amplitude) variable. These include coherent states (which, approximately, is what comes out of a laser), thermal states (like a lightbulb), vacuum states (no photons - but still some noise due to Heisenberg), and squeezed states (non-classical states with many applications in QIP). 

As well as Gaussian states, there are also Gaussian operations (phase shifts, beamsplitting, etc.) and measurements (homodyne, heterodyne) which are those operations/measurements that maintain the Gaussianity of the system's state. 

There is a wonderfully elegant formalism for  Gaussian states, operations and measurement. Jonatan Bohr Brask from QPIT wrote a very handy 10-page overview of the most important concepts, states and operations: [Gaussian states and operations – a quick reference](https://arxiv.org/abs/2102.05748). You won't have time to read it all now, but you can find most of the formulas you need for this exercise in there. For a more authoritative and in-depth review of the field, [Weedbrook et al.](https://journals.aps.org/rmp/abstract/10.1103/RevModPhys.84.621) is a go-to reference.

From a quantum computational perspective, however, Gaussian states are not so exciting: The wonderfully elegant formalism also allows for efficient classical simulation of Gaussian systems, meaning there's no quantum advantage to be found there. For many interesting applications, like quantum computing, we need to go non-Gaussian. 

Continuous variable quantum information gets a lot more murky when going beyond Gaussianity. In all modesty, I think [my own PhD thesis](https://figshare.com/articles/thesis/Generation_of_single_photons_and_Schr_dinger_kitten_states_of_light/1328405?file=1939711) does a good job of introducing the basics of quantum states in the infinite-dimensional Hilbert space representing the quantum harmonic oscillator. It includes formalism that allows for representing both Gaussian and non-Gaussian states, in particular the density matrix and the Wigner function and the correspondence between them. Sections 2.1 and 2.2 should be all you will need for this exercise.

### Suggestions for things to investigate & present

* The photon number distribution for Fock (number) states $|n\rangle$, coherent states $|\alpha\rangle$, squeezed states, etc.  
$p(n) = |\langle n|\psi\rangle|^2$ for pure states and $p(n) = \rho_{nn} = 2\pi \int\int_{-\infty}^{\infty}W(x,p)W_{|n\rangle\langle n|}(x,p) dxdp$ in general.
* Plotting the Wigner function for different states.
* Animating/interactively visualising the Wigner function of states undergoing symplectic transformations like displacement, rotation, squeezing.
* Implement the numerical conversion between density matrices and Wigner functions (my thesis, p.10). Density matrices in the Fock basis needs to be cut-off at a certain maximum photon number. This can introduce numerical issues for states like the coherent or squeezed states that have support on the full Hilbert space. See what happens if you convert a density matrix with a too low cutoff to its Wigner function. 

### Instructions for submission

Instead of just sharing your notebook on Discord, you will practice a Github pull request workflow:

1. On Github, create a fork of https://github.com/qpit/sciqis ("Fork" button near top right).
2. You now have a fork of the course repository under your own Github account. Clone this to your PC from your code editor or from the terminal with `git clone git@github.com:<your_github_username>/sciqis.git` or `git clone https://github.com/<your_github_username>/sciqis.git` (depending on your authorisation method).
3. Create a branch (any name _branch_name_) with the purpose of contributing your tutorial notebook to the sciqis repository:  
   ```
   git checkout submissions
   git checkout -b <branch_name>
   ```
1. Place your (mostly) finished notebook in the `/exercises/cv_submissions` folder. Name it exactly like this: `cv_tutorial_<name>.ipynb`  where `<name>` should preferably be your real name, but if you prefer not to use it (the notebook will appear on a public repository), it's ok to also use your github username instead. I.e. in my case, _cv_tutorial_jonas.ipynb_ or _cv_tutorial_neago.ipynb_.
2. Commit the notebook to the new branch of your repository. Make sure you didn't add anything else than this notebook:  
   ```
   git add cv_tutorial_<name>.ipynb
   git commit -m "Added my notebook"
   ```
3. Push it to your forked repository, `git push -u origin <branch_name>`.
4. Going to your forked repository on Github, switch to your new branch. You should now see a green button  called "Compare & pull request" or similar. Choose `submissions` as the branch to merge into. Complete the form (quick title and description, nothing fancy - would be good to include your name or username in the description) and Create Pull Request. Detailed instructions are [here](https://docs.github.com/en/pull-requests/how-tos/create-pull-requests/creating-a-pull-request). 
5. Confirm that the pull request is visible in the main course repository: https://github.com/qpit/sciqis/pulls

In case this doesn't work at all, the fallback solution is to send your notebook to me by direct message on Discord.