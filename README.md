# Project Task Summary

## Team Contributions

- **Seziberagabriel**: 
  - Task: Deleted the useless file `test-1` from the data directory.
    ```bash
    rm data/test-1
    ```

- **Ksheilla**: 
  - Task: Moved the file `top-5-lowest-temparatures.csv` from the root directory to the analyzed directory.
    ```bash
    mv top-5-lowest-temparatures.csv analyzed/
    ```

- **Allia-wase**: 
  - Task: Renamed the existing analyzed file to match the naming convention.
    ```bash
    mv analyzed/existing_analyzed_file.csv analyzed/top-5-existing_analyzed_file.csv
    ```

- **Sheilla**: 
  - Task: Checked for duplicate rows in the `satelite_temperature_data.csv` file and removed them.
    ```bash
    sort -u data/satelite_temperature_data.csv -o data/satelite_temperature_data.csv
    ```

- **Evand3rr**: 
  - Task: Extracted the top 5 highest temperatures.
    ```bash
    sort -t, -k2 -nr data/satelite_temperature_data.csv | head -n 6 > analyzed/top-5-highest-temparatures.csv
    ```

- **Batonicarla**: 
  - Task: Extracted the top 5 lowest temperatures.
    ```bash
    { head -n 1 satelite_temperature_data.csv && tail -n +2 satelite_temperature_data.csv | sort -t, -k2 -nr | head -n 5; } > analyzed/top-5-lowest-temperatures.csv
    ```

- **Supserrr**: 
  - Extra Task: Extracted data for your country and saved it in a new file named `country-heat_data.csv`.
    ```bash
    grep 'Rwanda' data/satelite_temperature_data.csv > analyzed/country-heat_data.csv
    ```
