# Written Tutorial

## Prerequisites
1. Ensure that your iNOC VPN IP Address has been whitelisted in the tool. If you have not previously requested this, please submit a ME ticket to Versa US Engineering Support and provide your iNOC VPN IP Address (this can be found on the FortiClient app once you connect to your VPN). 
2. Download the [SpeakerCountQueryTool.zip](https://latroservices962.sharepoint.com/:u:/s/tbu/Ef3goiQZJThCuf2eba1licUB0F-gJX2q03wKBiTkj8fWZg?e=Ib7re2)
3. Save and unzip the folder on your local machine

## Running the Tool
1. Connect to your iNOC VPN
2. Go to the location where the unzipped tool folder has been saved
3. Create a CSV file called "msisdns.csv" and enter all MSISDN values that you would like to search on (1 MSISDN per line)
4. Right click on the folder and select "Open in Terminal"
5. Within Powershell, type .\\SpeakerCountQueryTool.exe -i .\\msisdns.csv -e "YYYY-MM-DD" -d # -a 10.100.23.203 -m .\\TrainedRegressionModel.xml
*Note: Update the timestamp with the desired end time for your search*
*Note: Update # with the number of days you wish to search (max availability is 15 days)*
7. Click Enter to run the command
8. The output file will be saved to the same folder location as "speaker_counts.csv"

## Helpul Notes
1. For more information on the available arguments and shortcuts type .\\SpeakerCountQueryTool.exe -h
2. Speaker counts are stored for the last 15 days (current day -15)
