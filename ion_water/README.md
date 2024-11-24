The folders here have the data used to parameterize and validate the ion-water
and ion-ion interactions in CMM. All data is computed with wB97X-V/def2-QZVPPD. An example input stub is available, `example_input_eda.in`, to ensure calculations are easily reproducible.

- aimd: Coordinates and EDA outputs in CSV format. AIMD is run with wB97XV/def2-TZVPPD. Sampled
structures are re-labeled with wB97XV/def2-QZVPPD.

- mbe_data: Dimer and trimer structures of water or water with an ion sampled from clusters. The
structures were minimized with GFN2-XTB using Crest to locate the minima then reoptimized with
wB97X-V/def2-TZVPPD. All CSV files contain the output of EDA calculations with wB97XV/def2-QZVPPD.
The file ion_water_mbe_eda_wb97xv_qzvppd.xyz contains all of the wB97X-V optimized minima and the
CSV file contains the output of EDA calculations and a breakdown of the many-body contributions.

- mbx_comparison: CSV files with the 2-body and 3-body energies predicted by CMM, MBX, and AMOEBA
over the MBX test sets. See https://github.com/paesanilab/Data_Repository for structures.

- wb97xv_tzvppd_optimized_samples: Has a more granular breakdown of the structures contained in the file
ion_water_mbe_eda_wb97xv_qzvppd.xyz

- train_test_splits: Shows the specific train/test splits used in parameterizing the ions.
250 structures are drawn randomly from the aimd and mbe_data folders resulting in 750
total structures for fitting since both dimers and trimers are drawn from the clusters.

- ion_ion_water_scans: Scans of ion-pairs with and without an extra water molecule. Scans are relaxed.
