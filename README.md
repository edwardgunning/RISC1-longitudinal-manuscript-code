Code for the paper ‘A Multivariate Longitudinal Functional Model for
Repeatedly-Observed Human-Movement Data’
================

## Repository Structure:

------------------------------------------------------------------------

- :open_file_folder: **code**
  - :open_file_folder: **analysis** – scripts used to perform the data
    analysis.
    - :page_facing_up: [01 - Create Plot for
      Introduction](code/analysis/01-introduction-plot.R)
    - :page_facing_up: [02 - Create Plot of Stride
      Timings](code/analysis/02-strides-timing-plot.R)
    - :page_facing_up: [03 - Prepare Data for
      Analysis](code/analysis/03-data-preparation.R) ([extra
      figures](code/analysis/03-data-preparation-extra-plot.R))
    - :page_facing_up: [04 - Split Data into Test and Training
      Samples](code/analysis/04-test-train-split.R)
    - :page_facing_up: [05 - mv-FPCA basis
      Representation](code/analysis/05-basis-representation.R)
    - :page_facing_up: [06 - Linear Mixed Models of mv-FPCA
      Scores](code/analysis/06-scores-modelling.R) ([extra
      figures](code/analysis/06))
    - :page_facing_up: 07 - Individual Random Effects Analysis ([Script
      1](code/analysis/07-individual-fitted-mv-FPC1.R), [Script
      2](code/analysis/07-individual-analysis-predictions.R), [Script
      3](code/analysis/07-individual-analysis-test-error.R), [Script
      4](code/analysis/07-individual-analysis-changes.R))
    - :page_facing_up: 08 - Fixed Effects Analysis ([Script
      1](code/analysis/08-fixef-results-post-processing.R), [Script
      2](code/analysis/08-fixef-spline-coef.R))
  - :open_file_folder: **functions** – custom functions for modelling
    data analysis.
    - :page_facing_up: [Centering a (multivariate) object around a
      different mean](code/functions/center_fd_around_new_mean.R)
    - :page_facing_up: [Decentering a (multivariate) object around a
      different mean](code/functions/decenter_fd_around_new_mean.R)
    - :page_facing_up: [Helper functions for manipulating `fd`
      objects](code/functions/functions-helper-smoothing.R)
    - :page_facing_up: [Project (multivariate) functional data (`fd`
      object) onto (multivariate) FPCs (`pca.fd`
      object)](code/functions/project_data_onto_fpcs.R)  
    - :page_facing_up: [Computing the (%) of Variance Explained by a
      mv-FPCA
      reconstruction](code/functions/variance_explained_reconstruction.R)
    - :page_facing_up: [Custom theme for
      figures](code/functions/theme_gunning.R)
    - :page_facing_up: [Functions to generate data from a multilevel
      longitudinal design for the
      simulation](code/functions/generate_design.R)
    - :page_facing_up: [Generate data from a polynomial scalar
      longitudinal model for the
      simulation](code/functions/generate_polynomial_model_basis_coefficient.R)
    - :page_facing_up: [Generate multiple basis coefficients (i.e.,
      mv-FPC scores) from a polynomial scalar longitudinal model for the
      simulation](code/functions/generate-basis-coefficient-matrix.R)
    - :page_facing_up: [Construct an `fd` object by combining pca.fd
      object and matrix of PCA
      scores](code/functions/construct_fd_from_scores.R)
    - :page_facing_up: [Generate smooth Gaussian noise to add to
      simulated functional
      data](code/functions/function-generate-smooth-noise.R)
    - :page_facing_up: [Modified version of `pca.fd()` to choose $K$
      based on proportion of variance
      explained.](code/functions/pca.fd_pve_cutoff.R)
    - :page_facing_up: [Wrapper function to extract FPCA scores from a
      `pca.fd()` object and add them to a data
      frame.](code/functions/add_pca.fd_scores_to_df.R)
    - :page_facing_up: [Function to fit a polynomial scalar longitudinal
      model the to mv-FPC scores.](code/functions/fit_poly.R)
    - :page_facing_up: [Function to fit a “naive” model the to mv-FPC
      scores.](code/functions/fit_naive_spline_intercept.R)
    - :page_facing_up: [Function to fit a ml-FPCA model the to mv-FPC
      scores.](code/functions/fit_fpca.R)
    - :page_facing_up: [Function to fit a natural spline model the to
      mv-FPC scores.](code/functions/fit_spline.R)
    - :page_facing_up: [Reduced version of the above
      model.](code/functions/fit_spline_subject_ri_side.R)
    - :page_facing_up: [Function to calculate average integrated squared
      prediction error for functional
      observations.](code/functions/calculate_prediction_error.R)
    - :page_facing_up: [Function to calculate individual integrated
      squared prediction errors for functional
      observations.](code/functions/calculate_individual_prediction_errors.R)
    - :page_facing_up: [Convenience function to split data into train
      and test in simulation.](code/functions/split_train_test.R)
    - :page_facing_up: [Convenience function to load all functions
      needed in the
      simulation.](code/functions/source_all_simulation_functions.R)
    - :page_facing_up: [Convenience function to add polynomial terms to
      a data frame.](code/functions/add_poly_to_df.R)
    - :page_facing_up: [Convenience function to add natural spline terms
      to a data frame.](code/functions/add_natural_splines_to_df.R)
    - :page_facing_up: [Function to extract fixed-effects coefficients
      from a list of fitted `lmerMod`
      objects.](code/functions/extract_fixef_coef.R)
    - :page_facing_up: [Conveninence function to load all functions for
      data analysis.](code/functions/source_all_analysis_functions.R)
    - :page_facing_up: [Conveninence functions for post processing
      results.](code/functions/post-processing-functions.R)
    - :page_facing_up: [Function to calculate rate of change in
      longitudinal direction](code/functions/calculate_rate_of_change.R)
  - :open_file_folder: **tests** – some basic tests for the custom
    functions.
    - :page_facing_up: [Test for
      `center_fd_around_new_mean()`](code/functions/tests/test-center_fd_around_new_mean.R)
    - :page_facing_up: [Test for
      `decenter_fd_around_new_mean()`](code/functions/tests/test-decenter_fd_around_new_mean.R)
    - :page_facing_up: [Test for
      `variance_explained_reconstruction()`](code/functions/tests/test-variance-explained-reconstruction.R)
    - :page_facing_up: [Test for
      `generate_design_multiple_subjects()`](code/functions/tests/test-generate-design.R)
    - :page_facing_up: [Test for
      `generate_polynomial_model_basis_coefficient()`](code/functions/tests/test-generate_polynomial_model_basis_coefficient.R)
    - :page_facing_up: [Test 1 for
      `generate_basis_coefficient_matrix()`](code/functions/tests/test-generate-basis-coefficient-matrix-01.R)
    - :page_facing_up: [Test 2 for
      `generate_basis_coefficient_matrix()`](code/functions/tests/test-generate-basis-coefficient-matrix-02.R)
    - :page_facing_up: [Test for
      `construct_fd_from_scores()`](code/functions/tests/test_construct_fd_from_scores.R)
    - :page_facing_up: [Tests for
      `calculate_rate_of_change()`](code/functions/tests/test_calculate_rate_of_change.R)
    - :page_facing_up: [Tests for
      `calculate_individual_prediction_errors()`](code/functions/tests/test_calculate_individual_prediction_errors.R)
- :open_file_folder: **outputs**
  - :open_file_folder: **tables** – tables containing data-analysis
    results. Some are stored as `.csv` files while others have been
    exported to $TeX$ using `{xtable}` for inclusion in the paper.
  - :open_file_folder: **figures** – figures for the manuscript, all
    created in $TeX$ using `{tikzDevice}` and linked to overleaf, where
    the file [figures.tex](outputs/figures/figures.tex) compiles all the
    individual $TeX$ files.
  - 💾 also contains `.rds` objects saved at various stages of the data
    analysis
- :open_file_folder: **data** – contains the main dataset used in
  analysis and small data sets used to create the introduction and
  stride-timing plots.
