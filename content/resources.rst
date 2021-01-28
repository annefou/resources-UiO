What's your style?
------------------

To get started, you can use Jupyter (4) and VDI (3) which are good for developing and prototyping. 
Then to scale up, you can use the Sigma2 options: 6, 7, 8 which have access to the same data.  If you need the most power or flexibility, use `the services from the Norwegian e-infrastructure for Research & Education (Sigma2) <https://www.sigma2.no/>`_ for your data storage and computation (`Apply for Sigma2 resources <https://www.sigma2.no/apply-e-infrastructure-resources>`_ and `account required <https://www.metacenter.no/user/application/form/notur/>`_ for 4-8).
 
If you need simple applications with a graphical interface, try 3 (VDI).

If you use your own laptop/desktop (1, 2), then it's good for getting started but you have to copy your data and code back and forth once you need to scale up.

Summary table for remote data analysis workflows
------------------------------------------------

   * Good for data security: 3, 4, 5, 6, 8
   * Good for prototyping, working on the go, doing tests, interactive work: 1, 2, 3, 4, 5
   * Shares Triton data (e.g. scratch folders): 3, 4, 5, 6, 8
   * Easy to scale up, shares software, data, etc: 4, 5, 6, 8
   * Largest resources available 8 (medium: 6)
   * GPUs resources available 7 (and to some extent 8)


.. list-table::
   :header-rows: 1

   * * Workflow
     * Pros
     * Cons
     * Recommendation
     * UiO data (home & `astra <https://www.uio.no/english/services/it/research/storage/researchers.html>`_) Y/N
   * * 1. Own laptop/desktop computer
     * Can work from anywhere. Does not require internet connection.  You are in control.
     * Not good for personal or confidential data. Computing resources might not be enough. Accessing large data remotely stored at UiO might be problematic - you will end up having to copy a lot.  You have to manage software yourself.
     * Excellent for prototyping, working on the go, doing tests, interactive work (e.g. making figures). Don’t use it with large data or confidential / personal data.
     * N
   * * 2. UiO laptop
     * Same as above, plus same tools available as UiO employer. The list of tools pre-installed on your laptop usually may depends on your institute or department or local group policy (in particular for some paid software).
     * Same as above.
     * Same as above.
     * N
   * * 3. Remote virtual machine (https://view.uio.no/)
     * Computing happens on remote. Data access happens on remote, so it is more secure.
     * Computing resources are limited.
     * Excellent for prototyping, working on the go, doing tests, interactive work (e.g. making figures). More secure access to data.
     * Y
   * * 4. UiO Jupyterhub (https://jupyterhub.uio.no/)
     * Cloud based - resume work from anywhere.  Includes command line (#6) and batch (#7) easily.  Local data can be copied (a procedure is available if this service is used for teaching) but no access to your UiO data.
     * Jupyter can `become a mess if you aren't careful <https://scicomp.aalto.fi/scicomp/jupyter-pitfalls.html>`__.  You need to plan to scale up with #7 eventually, once your needs increase.
     * Excellent for prototyping, working on the go, doing tests, interactive work (e.g. making figures).  Secure access to data. Use if you know you need to switch to batch jobs eventually (7).
     * Y
   * * 5. Interactive graphical session on `UiO servers <https://www.uio.no/english/services/it/research/hpc/freebee/>`_ (ssh -X freebio.hpc.uio.no or on request to bioint01.hpc.uio.no)
     * Graphical programs.
     * Lost once your internet connection dies, needs fast internet connection.
     * If you need specific graphical applications   which are only on Triton.
     * N
   * * 6. Interactive command line session on UiO servers (ssh login.uio.no)
     * Works from anywhere. Few resources and for a short time.
     * Limited time limits, must be used manually.
     * A general workhorse once you get comfortable with shell - many people work here + #7.
     * Y
   * * 7. `GPU / Machine learning resources <https://www.uio.no/tjenester/it/forskning/kompetansehuber/uio-ai-hub-node-project/it-resources/ml-nodes/index.html>`_
     * Works from anywhere. Dedicated to machine learning and deep learning tasks.
     * No time limits
     * Only if your applications can use GPUs
     * N
   * * 8. Non-interactive batch HPC computing on Sigma2 (ssh + sbatch)
     * Largest resources, bulk computing
     * Need to script your computation
     * When you have the largest computational needs.
     * N
