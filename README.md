# Scalable Checkpoint / Restart (SCR) Library

The Scalable Checkpoint / Restart (SCR) library enables MPI applications
to utilize distributed storage on Linux clusters to attain high file I/O
bandwidth for checkpointing and restarting large-scale jobs. With SCR,
jobs run more efficiently, recompute less work upon a failure, and reduce
load on critical shared resources such as the parallel file system.

Detailed usage is provided at [SCR.ReadTheDocs.io](https://scr.readthedocs.io/en/latest/).

For new users, the [Quick Start guide](https://scr.readthedocs.io/en/latest/users/quick.html)
shows one how to build and run an example using SCR.

[![User Docs Status](https://readthedocs.org/projects/scr/badge/?version=latest)](https://scr.readthedocs.io/en/latest/?badge=latest)

## Contribute

As an open source project, we welcome contributions via pull requests, as well as questions, feature requests, or bug reports via issues.
Please refer to both our [code of conduct](CODE_OF_CONDUCT.md) and our [contributing guidelines](CONTRIBUTING.md).

## Developers

Developer documentation is provided at [SCR-dev.ReadTheDocs.io](https://scr-dev.readthedocs.io/en/latest/).

[![Developer Docs Status](https://readthedocs.org/projects/scr-dev/badge/?version=latest)](https://scr-dev.readthedocs.io/en/latest/?badge=latest)

SCR uses components from [ECP-VeloC](https://github.com/ECP-VeloC),
which have [user](https://github.com/ECP-VeloC/component-user-docs)
and [developer](https://github.com/ECP-VeloC/component-dev-docs) docs.

For a development build of SCR and its dependencies,
one can use the bootstrap.sh script:

    git clone git@github.com:llnl/scr.git
    cd scr

    ./bootstrap.sh --dev --debug

    cd build
    cmake -DCMAKE_INSTALL_PREFIX=../install ..
    make install

One can then run a test program:

    cd examples
    srun -n4 -N4 ./test_api

## Authors

Numerous people have [contributed](https://github.com/llnl/scr/graphs/contributors) to the SCR project.

To reference SCR in a publication, please cite the following paper:

* Adam Moody, Greg Bronevetsky, Kathryn Mohror, Bronis R. de Supinski, [Design, Modeling, and Evaluation of a Scalable Multi-level Checkpointing System](http://dl.acm.org/citation.cfm?id=1884666), LLNL-CONF-427742, Supercomputing 2010, New Orleans, LA, November 2010.

Additional information and research publications can be found here:

[http://computation.llnl.gov/projects/scalable-checkpoint-restart-for-mpi](http://computation.llnl.gov/projects/scalable-checkpoint-restart-for-mpi)
