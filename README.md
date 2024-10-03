# learn_linux_by_doing
Gabriel worked on the task of deleting the useless file test-1 from the data directory
rm data/test-1
Sheilla worked on the task of moving the top-5-lowest-temparatures.csv file from the root directory to the analyzed directory
mv top-5-lowest-temparatures.csv analyzed/
Alline worked on the task of renaming the existing analyzed file to match the naming convention
mv analyzed/existing_analyzed_file.csv analyzed/top-5-existing_analyzed_file.csv
Sheilla worked on the task of checking for duplicate rows in the satelite_temperature_data.csv file and remove them
sort -u data/satelite_temperature_data.csv -o data/satelite_temperature_data.csv
Evand3rr worked on the task to extract the top 5 highest temperatures
sort -t, -k2 -nr data/satelite_temperature_data.csv | head -n 6 > analyzed/top-5-highest-temparatures.csv
Carla worked on the task to extract the top 5 lowest temperatures
 { head -n 1 satelite_temperature_data.csv && tail -n +2 satelite_temperature_data.csv | sort -t, -k2 -nr | head -n 5; } > ../analyzed/top-5-highest-temperatures.csv
 Supserr worked on the extra task to extract data for your country and saved it in another new file and name it country-heat_data.csv
 grep 'Rwanda' data/satelite_temperature_data.csv > analyzed/country-heat_data.csv
