# ARIMA-And-Seasonal-ARIMA

<img src="https://www.google.com/imgres?imgurl=https%3A%2F%2Fi.stack.imgur.com%2FNUA6V.png&imgrefurl=https%3A%2F%2Fstats.stackexchange.com%2Fquestions%2F129901%2Fsarima-model-equation&tbnid=EATirDybW7OUgM&vet=12ahUKEwiVhqamvKfuAhUMpBoKHVbMCXoQMygBegUIARCkAQ..i&docid=pZKFKo8SG4C1KM&w=1169&h=317&q=arima%20and%20sarima&ved=2ahUKEwiVhqamvKfuAhUMpBoKHVbMCXoQMygBegUIARCkAQ" width="600" height="200" />
Let’s Break it Down:-
- AR: Autoregression. A model that uses the dependent relationship between an observation and some number of lagged observations.
- I: Integrated. The use of differencing of raw observations in order to make the time series stationary.
- MA: Moving Average. A model that uses the dependency between an observation and a residual error from a moving average model applied to lagged observations.

The parameters of the ARIMA model are defined as follows:
- p: The number of lag observations included in the model, also called the lag order.
- d: The number of times that the raw observations are differenced, also called the degree of differencing.
- q: The size of the moving average window, also called the order of moving average.

### This is all about ARIMA so…… What is SARIMAX?
The difference between ARIMA and SARIMA (SARIMAX) is about the seasonality of the dataset. if your data is seasonal, like it happen after a certain period of time. then we will use SARIMA.

### STATSMODEL
It primarily comprises of three main modules:

tsa– Comprises of functions useful for univariate time series analysis – autoregressive models (AR), vector autoregressive models (VAR), and univariate autoregressive moving average models (ARMA), along with Non-linear models like dynamic regression and autoregression. In addition, it also provides autocorrelation, partial autocorrelation function, periodogram, and other statistical properties related to ARMA, and methods that process moving average lag-polynomials.


statespace –  Equipped with functionality to model observations at any time instant with unobserved state vectors and irregular components. It has added flexibility to allow estimation with missing observations, forecasting, impulse response functions, etc. This flexibility helps it to differentiate from tsa by estimating additive and multiplicative seasonal effects on models (both on univariate and multi-variate), as well as arbitrary trend polynomials.

vector_ar-Allows simultaneous modeling and analyzing multiple time series.

ARIMA MODELS
An ARIMA model is composed of 3 constituent units which are :
AR: Autoregression. This part explores any dependent relationship between an observation and some number of lagged variables.
I: Integrated. This part aims to make time-series stationery by subtracting or differencing an observation from observation at the previous time step of the same time series.
MA: Moving Average. This part explores the relationship between an observation and a residual error by application of moving average to lagged observations, with any given time window.

In order to design a model (say ARIMA) by applying all of the above stated procedures we need to enable all parameters. We can also enable partial parameters and select to choose either AR or MA model. The parameters can be summarized as follows:

p: The number of lag observations included in the model, also called the lag order.

d: The number of times that the raw observations are differenced also called the degree of difference.

q: The size or the order of the moving average window.

To start with and in order to have different flavours of ARIMA model, the library imports are:


from statsmodels.tsa.ar_model import AR
from statsmodels.tsa.arima_model import ARIMA
from statsmodels.tsa.statespace.sarimax import SARIMAX
from statsmodels.graphics.tsaplots import plot_acf,plot_pacf
