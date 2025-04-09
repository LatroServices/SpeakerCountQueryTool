# Written Tutorial

## Prerequisites
1. Ensure that your iNOC VPN IP Address has been whitelisted in the tool. If you have not previously requested this, please submit a ME ticket to Versa US Engineering Support and provide your iNOC VPN IP Address (this can be found on the FortiClient app once you connect to your VPN). 
2. Download the [SpeakerCountQueryTool.zip](https://latroservices962.sharepoint.com/:u:/s/tbu/EWmEkwouuUNMvsIhf3_xYDkBsspuiq5nmDv4ARRSW3xtiA?e=JUAXDG)
3. Save and unzip the folder on your local machine

## Running the Tool
1. Connect to your iNOC VPN
2. Go to the location where the unzipped tool folder has been saved
3. Create a CSV file called "msisdns.csv" and enter all MSISDN values that you would like to search on (1 MSISDN per line)
4. Right click on the folder and select "Open in Terminal"
5. Within Powershell, type .\\SpeakerCountQueryTool.exe -i .\\msisdns.csv -e "YYYY-MM-DD HH:MM:SS" -a 10.100.23.203 -m .\\TrainedRegressionModel.xml
*Note: Update the timestamp with the desired end time for your 24 hour search*
6. Click Enter to run the command
7. The output file will be saved to the same folder location as "speaker_counts.csv"

## Helpul Notes
1. For more information on the available arguments and shortcuts type .\\SpeakerCountQueryTool.exe -h
2. Run multiple commands with changing the timestamp to view results over a longer interval than 24 hours
