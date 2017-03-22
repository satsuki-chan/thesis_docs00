# Documents and files with all downloaded mutual funds information used in the research for the thesis:
## *"Comparison between traditional risk measurement methods and machine learning methods in Mexican equity investment funds"*
### required to obtain the grade of **Master of Software Engineering**, at *Centro de Investigación en Matemáticas, A.C.*, Zacatecas Unit.

## List of files:
### Mutual funds downloaded from the [**National Banking and Stock Commission**](http://www.cnbv.gob.mx/SECTORES-SUPERVISADOS/SOCIEDADES-DE-INVERSION/Buscador-de-Sociedades-de-Inversi%C3%B3n/Paginas/Buscador-de-Sociedades-de-Inversion.aspx) (CNBV, *Comisión Nacional Bancaria y de Valores*) website
* `RVMexico.fondos_a_analizar_20160127.xlsx`
#### Sheets contents:
 * **Fondos-CNBV**. Complete list of Mexican mutual funds registered at the CNBV website, until October, 2015.
 * **FondosRVMexico-CNBV_seleccion01**. First selection of Mexican equity to analyse.
 * **FondosRVMexico-CNBV_seleccion02**. Second and final selection of Mexican equity to analyse.
 * **FondosRVMexico-CNBV_seleccion02_correccionSB**. Equity funds with missing benchmark in the CNBV, but with existing benchmark in the [Morningstar Mexico](http://www.morningstar.com.mx) website.
 * **FondosRVMexico-CNBV_problemas**. List of equity excluded form the second funds selection and their causes.

### Compilation of traditional and novel machine learning risk analysis results for the analyzed (182) equity funds
* `RVMexico.fondos_capm_analysis_CORT_pclust_20160908165248.xlsx`

### Traditional risk analysis with **Modern Portfolio Theory** (MPT) statistics: alpha, beta, r squared, standard deviation and Sharpe ratio
* `RVMexico.capm_analysis_20160908165248.xlsx`
##### In .csv format:
 * `RVMexico.capm_analysis_20160908165248.csv`

### Equity funds dissimilarity CORT values and clustering results, in matrix format
* `RVMexico.tsclust_analysis_CORT.xlsx`
##### In .csv format:
 * `RVMexico.tsclust_analysis_CORT_20160504234444.csv`
 * `RVMexico.tsclust_analysis_CORT_pclust_20160504234444.csv`

### Input file for script to generate the scatter plots graphs of the comparissions of the MPT statistics from Mexican equity funds, grouped by the CORT clustering analysis (see [**"Thesis Repository 06 - Scatter plots of Mexican equity funds' Modern Portfolio Theory variables comparison"**](https://github.com/satsuki-chan/ananov_tsclust_graph06))
* `RVMexico.capm_pclust_20160908165248.csv`

## List of directories:
* `0 - Raw data backup from Yahoo! Finanzas`. Backup of the raw files with the equity funds historical price information downloaded form the Yahoo! Fianzas web portal.
  * Notes:
    1. All data in files `found_data*.csv`, was downloaded with Python 2.7 yahoo-finance 1.2.1 library, which allows the search of stocks and mutual funds information from the Yahoo! Finanas web portal (the Spanish language version of the [**Yahoo! Finance**](https://es-us.finanzas.yahoo.com) web portal).
    2. Data in files `raw_found_data_<*>.csv` come from the manually searches and downloaded mutual funds from the Yahoo! Finanzas web portal. Due to having ticker symbols different from those officially registered at the CNBV website, those funds' price series couldn't be automatically donwloaded with the yahoo-finance library.
    3. Data in files `raw_found_data_extra_<*>.csv` come from manually downloaded mutual funds from the Yahoo! Finanzas web portal for months December, 2015, and January, 2016.
    4. Data in files `raw_consulta_banxico_<*>.csv` contain the daily rates of goverment issued debt instruments from the [Bank of Mexico](http://www.banxico.org.mx/) (Banxico, Banco de México) [Economic Information System](http://www.banxico.org.mx/SieInternet/consultarDirectorioInternetAction.do?sector=18&idCuadro=CF300&accion=consultarCuadro&locale=en).
* `1 - Data backup for analysis and experiments`. Backup of the tables of the MariaDB database used to store the downloaded historical price information and the results of the preprocesing phase.
* `2 - CORT analysis scatterplot graphs`. Backup of the scatter plots graphs of the comparissions of the MPT statistics from Mexican equity funds, grouped by the CORT clustering analysis.
