#!/bin/bash

	if [ testResults.csv ]; then
    		rm testResults.csv 
	fi
	for file in Graphs/*.mtx
	do
	 # do something on "$file"
		#file name is now like data/Matrix.mtx
		#the following lines are used to remove .mtx and /data	  
		#split file name using '.' delimeter 
		IFS='.'
		read -a direc <<< "${file}"
		#split file name using '.' delimeter 
		IFS='/'
		read -a name <<< "${direc}"

		./ColPack "$file" NATURAL COLUMN_PARTIAL_DISTANCE_TWO >> testResults.csv 
		./ColPack "$file" LARGEST_FIRST COLUMN_PARTIAL_DISTANCE_TWO >> testResults.csv 
		./ColPack "$file" SMALLEST_LAST COLUMN_PARTIAL_DISTANCE_TWO >> testResults.csv
		./ColPack "$file" INCIDENCE_DEGREE COLUMN_PARTIAL_DISTANCE_TWO >> testResults.csv
		./ColPack "$file" NATURAL ROW_PARTIAL_DISTANCE_TWO >> testResults.csv 
		./ColPack "$file" LARGEST_FIRST ROW_PARTIAL_DISTANCE_TWO >> testResults.csv 
		./ColPack "$file" SMALLEST_LAST ROW_PARTIAL_DISTANCE_TWO >> testResults.csv
		./ColPack "$file" INCIDENCE_DEGREE ROW_PARTIAL_DISTANCE_TWO >> testResults.csv
		#Put gcolor result and profilings in appropriate folders
		
	done
	echo "Done!!"

	#echo $1
	
	
 

