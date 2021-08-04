# PagePathViews

## Create the dataflow in your Tableau CRM

### Step 1
- Log in TCRM and find the Data Manager link
- Select the "Dataflows and Recipes" link

### Step 2: 
- Click on "Create Dataflow" ![Click on Create Dataflow](screenshots/ScreenShot-03.png)
- Select the name of your choice, for example "PPV_Dataflow" ![Select the name of your choice, for example PPV_Dataflow](screenshots/ScreenShot-04.png)

### Step 3: 
- Download the Dataflow JSON source from this repository at [/Dataflow.json](https://raw.githubusercontent.com/VinceFINET/PagePathViews/main/Dataflow.json)
- Select the fourth button to load the Dataflow JSON of this repository ![Select the fourth button to load the Dataflow JSON of this repository](screenshots/ScreenShot-05.png)
- Click on continue to confirm
- Select the Dataflow JSON file that you download previously.
- Click on "Update Dafaflow" and click again to launch it.

## Troubleshooting the Dataflow
- We assume that the dataset "LightningPageViewWithUsers" exists. You may need to update the "PPV_Edgemart_1" node (edgemart type) with the appropriate alias to use.
- The resulting dataset "PPV_LightningPathView" will be created the first time in the "Shared" application. Feel free to move it in another application in TCRM.
- Don't forget the schedule the dataflow after the one from Shield Event Monitoring application.

## Create your first lens
- After the dataset is created you can start construct a "Lens" based on "PPV_LightningPathView" for example group by "PPV_PagePath" and Order by count descending.
- Happy lensing and dashboarding!!!
