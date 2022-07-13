===================
Welcome to IgnisHPC
===================

IgnisHPC is a framework whose main objective is to unify the execution of Big Data and HPC workloads in the same computing engine. IgnisHPC has native support for multi-language applications using JVM and non-JVM-based languages. Currently it supports C, C++, Python, Java and Go.

Since MPI was used as its backbone technology, IgnisHPC allows MPI applications and libraries to be directly executed in an efficient way in the framework. In this way, most of the HPC scientific applications, which in many cases contain tens of thousands of lines of code, do not have to be ported to a new API or programming model. The main consequence is that **users could combine in the same multi-language code HPC tasks (using MPI) with Big Data tasks (using MapReduce operations)**.

IgnisHPC outperforms the state-of-the-art framework Spark in terms of performance and scalability running applications that represent the most typical algorithmic patterns in Big Data and scientific computing. For example, considering a 12-node cluster with 2 × Intel Xeon E5-2630v4 (2.2Ghz, 10 cores) per node, the experimental results show that:

+-------------------+-------------------+
| Application       | No. times faster  |
|                   | than Spark        |
+===================+===================+
| Minebench         | 3.9x [Python/C++] |
|                   | 1.3x [Python]     |
+-------------------+-------------------+
| Terasort          | 1.8x [C++]        |
|                   | 1.4x [Python]     |
+-------------------+-------------------+
| K-Means           | 1.9x [Python/C++] |
+-------------------+-------------------+
| PageRank          | 1.1x [Python]     |
+-------------------+-------------------+
| Transitive        | 1.12x [Python]    |
| Closure           |                   |
+-------------------+-------------------+


Documentation:

- IgnisHPC is a containerized framework, so all the system modules are executed inside Docker containers. More information about the installation can be found in `Getting started <https://ignishpc.readthedocs.io/en/latest/started.html#getting-started>`_.
- To facilitate the adoption from the Big Data community, the `IgnisHPC API <https://ignishpc.readthedocs.io/en/latest/api.html#>`_ was inspired by the Spark API in such a way that IgnisHPC codes are easily understandable by users who are familiar with Spark.
- Example of how to run an MPI application from IgnisHPC. More code examples can be found in our papers (see below).
- The complete documentation is `here <https://ignishpc.readthedocs.io/en/latest/>`_.

If you use IgnisHPC, please cite:

César Piñeiro and Juan C. Pichel. `A Unified Framework to Improve the Interoperability between HPC and Big Data Languages and Programming Models <http://dx.doi.org/10.1016/j.future.2022.04.002>`_. Future Generation Computer Systems, Vol. 134, pages 123-139, 2022.

César Piñeiro, Rodrigo Martínez-Castaño and Juan C. Pichel. `Ignis: An efficient and scalable multi-language Big Data framework <http://dx.doi.org/10.1016/j.future.2019.12.052>`_. Future Generation Computer Systems, Vol. 150, pages 705-716, 2020.


.. |core1| image:: https://raw.githubusercontent.com/ignishpc/docs/main/logos/svg/ignis-hpc-python.svg
   :alt: IgnisHPC core python
   :target: https://github.com/ignishpc/core-python

.. |core2| image:: https://raw.githubusercontent.com/ignishpc/docs/main/logos/svg/ignis-hpc-cpp.svg
   :alt: IgnisHPC core cpp
   :target: https://github.com/ignishpc/core-cpp

.. |core3| image:: https://raw.githubusercontent.com/ignishpc/docs/main/logos/svg/ignis-hpc-java.svg
   :alt: IgnisHPC core java
   :target: https://github.com/ignishpc/core-java

.. |core4| image:: https://raw.githubusercontent.com/ignishpc/docs/main/logos/svg/ignis-hpc-go.svg
   :alt: IgnisHPC core go
   :target: https://github.com/ignishpc/core-go


+---------------------+---------------------+---------------------+---------------------+
|       |core1|       |       |core2|       |       |core3|       |       |core4|       |
+---------------------+---------------------+---------------------+---------------------+
| **Python**          | **C/Cpp**           |**Java**             | **Go**              |
|                     |                     |(under revision)     | (alpha)             |
+---------------------+---------------------+---------------------+---------------------+
