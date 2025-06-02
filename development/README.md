<br>

* [Background](#background)
* [Model Development References](#model-development-references)
* [Environment & Engineering](#environment--engineering)
* [Snippets](#snippets)
* [NGINX, etc.](#nginx-etc)

<br>

## Background

* [Accident & Emergency](https://publichealthscotland.scot/our-areas-of-work/acute-and-emergency-services/urgent-and-unscheduled-care/accident-and-emergency/overview/#section-1)
* [Scottish Health and Social Care Open Data](https://www.opendata.nhs.scot/dataset)
  * [Weekly A&E Activity and Waiting Times](https://www.opendata.nhs.scot/dataset/weekly-accident-and-emergency-activity-and-waiting-times)
  * [Hospital Codes](https://www.opendata.nhs.scot/dataset/hospital-codes)
  * [Population Estimates](https://www.opendata.nhs.scot/dataset/population-estimates)
* [Assessment of Accident and Emergency (A&E) Activity Statistics in Scotland](https://osr.statisticsauthority.gov.uk/publication/assessment-of-accident-and-emergency-ae-activity-statistics-in-scotland/)
* [Five big problems the NHS in Scotland needs to fix](https://www.bbc.com/news/uk-scotland-64303425)


<br>
<br>


## Model Development References

Bayesian Machine Learning Properties
* [TensorFlow Probability](https://www.tensorflow.org/probability)
* [Bayesian Modelling Notes](https://github.com/plausibilities/delineating#notes)
* [Notation: State Space Model, Kalman Filter](https://dismalpy.github.io/user/ssm/2-state_space_models.html)
* [<abbr title="Markov Chain Monte Carlo">MCMC</abbr> Convergence Diagnostic](https://search.r-project.org/CRAN/refmans/LaplacesDemon/html/Gelman.Diagnostic.html)
* [Convergence and efficiency diagnostics for Markov Chains](https://mc-stan.org/rstan/reference/Rhat.html)
* [Effective Sample Size (ESS) due to Auto-correlation](https://search.r-project.org/CRAN/refmans/LaplacesDemon/html/ESS.html)
* [<abbr title="Monte Carlo Standard Error">MCSE</abbr>: Equation & References](https://search.r-project.org/CRAN/refmans/LaplacesDemon/html/MCSE.html)
* [Understanding and interpreting confidence and credible intervals around effect estimates](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6630113/)

<br>

Text
* [Statistical forecasting: notes on regression and time series analysis](https://people.duke.edu/~rnau/411home.htm)
  * [Identifying the order of differencing in an ARIMA model](https://people.duke.edu/~rnau/411arim2.htm)
  * [Identifying the numbers of AR or MA terms in an ARIMA model](https://people.duke.edu/~rnau/411arim3.htm)
* [Forecasting: Principles & Practice $\bigl(2^{ND}\; Edition\bigr)$](https://otexts.com/fpp2)

<br>

Forecasting
* [Stationarity and differencing](https://otexts.com/fpp2/stationarity.html)
* [Season-Trend decomposition using LOESS (locally estimated scatterplot smoothing)](https://www.statsmodels.org/dev/generated/statsmodels.tsa.seasonal.STL.html)
  * [Decomposition & Forecasting with STL](https://www.statsmodels.org/dev/examples/notebooks/generated/stl_decomposition.html)
  * [Decompose](https://www.statsmodels.org/dev/generated/statsmodels.tsa.seasonal.seasonal_decompose.html)
  * [Forecasting with decomposition](https://otexts.com/fpp2/forecasting-decomposition.html), [ARIMA (AutoRegressive Integrated Moving Average)](https://www.statsmodels.org/dev/generated/statsmodels.tsa.arima.model.ARIMA.html#statsmodels.tsa.arima.model.ARIMA)
  * [STL Forecast Class: Seasonal Trend LOESS  Forecast Class](https://www.statsmodels.org/dev/generated/statsmodels.tsa.forecasting.stl.STLForecast.html#statsmodels.tsa.forecasting.stl.STLForecast)
* [Seasonal ARIMA models](https://otexts.com/fpp2/seasonal-arima.html)
  * [Seasonal AutoRegressive Integrated Moving Average with eXogenous regressors model](https://www.statsmodels.org/stable/generated/statsmodels.tsa.statespace.sarimax.SARIMAX.html#statsmodels.tsa.statespace.sarimax.SARIMAX)
  * [Seasonal Autoregressive Integrated Moving Average](https://machinelearningmastery.com/sarima-for-time-series-forecasting-in-python/)
* [Non-seasonal ARIMA models](https://otexts.com/fpp2/non-seasonal-arima.html)
* [AutoRegression](https://blog.quantinsti.com/autoregression/)
* [Evaluating forecast accuracy](https://otexts.com/fpp2/accuracy.html), [Forecasting on training and test sets](https://otexts.com/fpp2/forecasting-on-training-and-test-sets.html)
* [Robust de-trending, re-referencing, outlier detection, and inpainting for multichannel data](https://pmc.ncbi.nlm.nih.gov/articles/PMC5915520/)
* [Using ARIMA and ETS models for forecasting water level changes for sustainable environmental management](https://www.nature.com/articles/s41598-024-73405-9)
* [Natural Logarithm Transformations](https://www.bridgetext.com/log-transforming-time-series-data-in-r)
* [Statistical forecasting: notes on regression and time series analysis](https://people.duke.edu/~rnau/411home.htm)
  * [Identifying the order of differencing in an ARIMA model](https://people.duke.edu/~rnau/411arim2.htm)
  * [Identifying the numbers of AR or MA terms in an ARIMA model](https://people.duke.edu/~rnau/411arim3.htm)


<br>

Stationarity
* [Stationarity and differencing](https://otexts.com/fpp2/stationarity.html)
* [Kwiatkowski-Phillips-Schmidt-Shin (KPSS) test for stationarity](https://www.statsmodels.org/dev/generated/statsmodels.tsa.stattools.kpss.html#statsmodels.tsa.stattools.kpss)
* [Stationarity and de-trending [ADF (Augmented Dickey Fuller)/KPSS]](https://www.statsmodels.org/dev/examples/notebooks/generated/stationarity_detrending_adf_kpss.html)

<br>

Auto-correlation
* [Ljung-Box test of auto-correlation in residuals](https://www.statsmodels.org/dev/generated/statsmodels.stats.diagnostic.acorr_ljungbox.html#statsmodels.stats.diagnostic.acorr_ljungbox)
* [Auto-correlation Function / Partial Auto-correlation Function](https://www.baeldung.com/cs/acf-pacf-plots-arma-modeling)
* Partial Auto Correlation Function: [1](https://www.statsmodels.org/stable/generated/statsmodels.graphics.tsaplots.plot_pacf.html), [2](https://www.itl.nist.gov/div898/handbook/pmc/section4/pmc4463.htm)

<br>

Additionally
* [Model Identification](https://www.itl.nist.gov/div898/handbook/pmc/section4/pmc4461.htm)
* [Robust de-trending, re-referencing, outlier detection, and inpainting for multichannel data](https://pmc.ncbi.nlm.nih.gov/articles/PMC5915520/)
* [Using ARIMA and ETS models for forecasting water level changes for sustainable environmental management](https://www.nature.com/articles/s41598-024-73405-9)
* [Natural Logarithm Transformations](https://www.bridgetext.com/log-transforming-time-series-data-in-r)

<br>
<br>

## Environment & Engineering

Alerting
* [Start workflow executions from a task state in Step Functions](https://docs.aws.amazon.com/step-functions/latest/dg/concepts-nested-workflows.html)
* [Deploy a state machine using a starter template for Step Functions](https://docs.aws.amazon.com/step-functions/latest/dg/starter-templates.html)

<br>

Monitoring
* [Process/Product Monitoring & Control](https://www.itl.nist.gov/div898/handbook/pmc/pmc.htm)
* [Variables Control Charts](https://www.itl.nist.gov/div898/handbook/pmc/section3/pmc32.htm)

<br>

Drift
* [Understanding Data Drift and Model Drift: Drift Detection in Python](https://www.datacamp.com/tutorial/understanding-data-drift-model-drift)
* [How To Detect Data Drift on Datasets](https://encord.com/blog/detect-data-drift/)

<br>

GIT
* [Demystifying the Git Commit Hash - A Beginner‘s Guide](https://thelinuxcode.com/git-commit-hash-and-how-to-get-it/)
* [Why you should pin your GitHub Actions by commit-hash](https://blog.rafaelgss.dev/why-you-should-pin-actions-by-commit-hash)

<br>

Graphing
* [pyplot.plot](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.plot.html)
* [matplotlib.markers](https://matplotlib.org/stable/api/markers_api.html#module-matplotlib.markers)
* [model_to_graphviz](https://www.pymc.io/projects/docs/en/stable/api/model/generated/pymc.model_graph.model_to_graphviz.html)
* [graphviz](https://graphviz.readthedocs.io/en/stable/index.html)

<br>

Parallel Computing
* [Parallelism](https://docs.deepmodeling.com/projects/deepmd/en/master/troubleshooting/howtoset_num_nodes.html)
  * [Runtime Variables](https://docs.deepmodeling.com/projects/deepmd/en/v3.0.0b4/env.html)
* [Parallel Processing (including terminology)](https://stat243.berkeley.edu/fall-2024/units/unit6-parallel.html)
* [TensorFlow Runtime (TFRT)](https://blog.tensorflow.org/2020/04/tfrt-new-tensorflow-runtime.html)
* Multi-processing
  [multiprocessing (python)](https://docs.python.org/3/library/multiprocessing.html)
  [Multiprocessing in Python](https://superfastpython.com/multiprocessing-in-python)
  [multiprocessing.pool.Pool()](https://superfastpython.com/multiprocessing-pool-python/)

<br>

JAX, XLA, etc.
* [OpenXLA (Open Accelerated Linear Algebra)](https://openxla.org)
* [Setting XLA Flags](https://docs.jax.dev/en/latest/xla_flags.html)
* [JAX](https://docs.jax.dev/en/latest/index.html)
* [GPU Performance Tips](https://docs.jax.dev/en/latest/gpu_performance_tips.html)
* [JAX: CPU, GPU, TPU](https://docs.jax.dev/en/latest/installation.html)
* [JAX NGC Container](https://catalog.ngc.nvidia.com/orgs/nvidia/containers/jax)
* [JAX Toolbox](https://github.com/NVIDIA/JAX-Toolbox)
* [Controlling data and computation placement on devices](https://docs.jax.dev/en/latest/faq.html#controlling-data-and-computation-placement-on-devices)
* [JAX & NUMPYRO Configuration](https://ringdown.readthedocs.io/en/latest/configuration.html)

<br>

BLAS, etc.
* [How do I configure/test my BLAS library](https://pytensor.readthedocs.io/en/latest/troubleshooting.html#how-do-i-configure-test-my-blas-library)
* [NUMBA](https://numba.readthedocs.io/en/stable/index.html), [Guide](https://numba.readthedocs.io/en/stable/user/5minguide.html)
* [MCMC for big datasets: faster sampling with JAX and the GPU](https://www.pymc-labs.com/blog-posts/pymc-stan-benchmark/)
* [numpyro.util](https://num.pyro.ai/en/stable/_modules/numpyro/util.html)

<br>

DASK
* [Scheduler](https://docs.dask.org/en/stable/scheduler-overview.html)

<br>


TENSORFLOW
* [Amazon EMR & TensorFlow](https://docs.aws.amazon.com/emr/latest/ReleaseGuide/emr-tensorflow.html)
* [TensorFlow & Docker](https://www.tensorflow.org/install/docker#examples_using_gpu-enabled_images)

<br>

## Snippets

Settings for computations


```bash
pytensor.config.blas__ldflags = '-llapack -lblas -lcblas'
```

```bash
pytensor.config.mode = 'NUMBA'
```

```bash
os.environ['OMP_NUM_THREADS'] = ''
```

```bash
os.environ['XLA_FLAGS'] = (
  '--xla_disable_hlo_passes=constant_folding '
  f'--xla_force_host_platform_device_count={} ')
```

Seasonal Component Modelling: Warnings
* ConvergenceWarning: Maximum Likelihood optimization failed to converge.
* OptimizeWarning: Desired error not necessarily achieved due to precision loss.

<br>

## NGINX, etc.

JavaScript Modules
* [Modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules)
* [Modules](https://javascript.info/modules)
* [Module Errors](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors/import_decl_module_top_level#importing_in_a_non-module_script)
* [SCRIPT](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script)

JavaScript
* [fetch](https://javascript.info/fetch)
* [1](https://wpdean.com/css-dropdown-menus/), [2](https://jsfiddle.net/cL2x7/), [3](https://www.geeksforgeeks.org/how-to-creating-html-list-from-javascript-array/)

live server
* [live server](https://itnext.io/dockerizing-modern-web-apps-cd9667eebf44)
* [github](https://github.com/tapio/live-server)
* [npm](https://www.npmjs.com/package/live-server)

NGINX
* [docker hub](https://hub.docker.com/_/nginx)
* [docker nginx](https://toxigon.com/setting-up-nginx-with-docker)
* [docker nginx](https://www.uptimia.com/questions/how-to-run-nginx-in-the-foreground-within-a-docker-container#implementing-the-solution-in-docker)
* [extra help](https://itnext.io/dockerizing-modern-web-apps-cd9667eebf44)
* [more](https://www.socketxp.com/iot/remote-access-nginx-web-server-from-internet/)
* [nginx -g 'daemon off;'](https://www.thecoderscamp.com/nginx-g-daemon-off/)
* [Dockerfile](https://github.com/devasthali-os/nginx-base/blob/master/Dockerfile)
* [conf](https://nginx.org/en/docs/beginners_guide.html#conf_structure)
* [MIME (Multipurpose Internet Mail Extensions) Types](https://server.hk/blog/14461/)
* [MIME Types](https://www.slingacademy.com/article/nginx-mime-types-the-complete-guide/)
* [load error example](https://www.slingacademy.com/article/nginx-error-cannot-load-css-js-files/)

Docker
* [docker run](https://docs.docker.com/reference/cli/docker/container/run/)

vim & vi
* [vi](https://linuxsimply.com/cheat-sheets/vi/)
* [vim](https://vim.rtorr.com)
* [vim](https://www.redhat.com/en/blog/beginners-guide-vim)

<br>
<br>
 
<br>
<br>
 
<br>
<br>
 
<br>
<br>
 