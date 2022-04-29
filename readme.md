
<h1 align="center"><strong>Monte Carlo simulations of Ising Model</strong></h>

</br>
</br>

![](IsingMCgif.gif)

## ABOUT

The program provides Monte Carlo simulations of 2D Ising model.

## CLI

    py main.py [-s|--seed <int>] [-L|--length <int>] [-T*|--temperature-reduced <float>] [-h|--external-magnetic-field <float>] [-J|--J|--interaction <float>] [-K|--K|--steps <int>] [-m|-m0|--initial-magnetization <float>] [-alg|--algorithm <string>] [-a|--animation [<char><char>]] [-sc|--save-configuration [<path>]] [-sm|--save-magnetization [<path>]]

## DESCRIPTION
`-s <int>`</br>
`--seed <int>`</br>
<div>
  <ul>
    A seed <code>&lt;int&gt;</code> for the random number generator in module "random".</br>
    The default is 1997.
  </ul>
</div>
</br>

`-L <int>`</br>
`--length <int>`</br>
<div>
  <ul>
    A length L=<code>&lt;int&gt;</code> of the lattice LxL in the system of spins.</br>
    The default is 10.
  </ul>
</div>
</br>

`-T* <float>`</br>
`--temperature-reduced <float>`</br>
<div>
  <ul>
    Reduced temperature T*=<code>&lt;float&gt;</code> of the system, where T*=1/(J x Beta).</br>
    The default is 1.0.
  </ul>
</div>
</br>

`-h <float>`</br>
`--external-magnetic-field <float>`</br>
<div>
  <ul>
    External homogenious magnetic field h=<code>&lt;float&gt;</code> of the system.</br>
    The default is 0.0.
  </ul>
</div>
</br>

`-J <float>`</br>
`--J <float>`</br>
`--interaction <float>`</br>
<div>
  <ul>
    Interaction J=<code>&lt;float&gt;</code> between a pair of spins.</br>
    The default is 1.0.
  </ul>
</div>
</br>

`-K <int>`</br>
`--K <int>`</br>
`--steps <int>`</br>
<div>
  <ul>
    Number of desired MCSs (iterations) K==<code>&lt;int&gt;</code>.</br>
    The default is 1.
  </ul>
</div>
</br>

`-m <float>`</br>
`-m0 <float>`</br>
`--initial-magnetization <float>`</br>
<div>
  <ul>
    Initiated magnetization m(t=0)=<code>&lt;float&gt;</code>.</br>
    The default is 0.0.
  </ul>
</div>
</br>

`-alg <string>`</br>
`--algorithm <string>`</br>
<div>
  <ul>
    An algorithm used by the Monte Carlo method to computing evolution of the system. Avaliable algorithms:</br>
        <div>
        <ul>
            <code>&lt;string&gt;</code>=='metropolis'</br>
            <code>&lt;string&gt;</code>=='glauberg'
        </ul>
        </div>
    The default is 'glauber'.
  </ul>
</div>
</br>

`-a [<char><char>]`</br>
`--animation [<char><char>]`</br>
<div>
  <ul>
    Turns on the visual evolution of the system. <code>&lt;char&gt;&lt;char&gt;</code> is a pair of characters that represents spin "up" and spin "down". The total time of execution will increase. Works only on Windows OS.</br>
    The default pair is U+0020, U+2588.
  </ul>
</div>
</br>

`-sc [<path>]`</br>
`--save-configuration [<path>]`</br>
<div>
  <ul>
    At the end of the simulation the configuration of spins S[ij] will be saved in a given directory <code>&lt;path&gt;</code>.</br>
    The dafault is "./".
  </ul>
</div>
</br>

`-sm [<path>]`</br>
`--save-magnetization [<path>]`</br>
<div>
  <ul>
    At the end of the simulation the time-dependent evolution of magnetization m(t) [MCS] of the system will be saved in a given directory <code>&lt;path&gt;</code>.</br>
    The dafault is "./" (the path of this module).
  </ul>
</div>

## REQUIREMENTS

    Python >= 3.10.2

## EXAMPLES

    py main.py -L 40 -T* 2.26 -a -alg "metropolis"
    py main.py -L 30 -m 1.0 -sc
    py main.py --seed 23 -K 3000 -sm "./data3/"