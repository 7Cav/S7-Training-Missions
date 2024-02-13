# S7-Training-Missions

## Automaticly update cScripts
Create a `setup.json` and place it in the root directory of your mission file.
```json
{
    "mission.sqm" : {
        "author" : "PFC Tully.B",
        "briefingName" : "Training Mission v$0",
        "overviewText" : "cScripts v$1 is installed on this mission."
    },
    "description.ext" : {
        "author" : "PFC Tully.B",
        "onLoadName" : "Training Mission v$0",
        "onLoadMission" : "7th Cavalry - S3 1BN Battle Staff Training",
        "onLoadIntro" : "S3 1BN Battle Staff Training",
        "CfgFunctions" : [],
        "add" : []
    },
    "init.sqf" : {
        "add" : []
    },
    "cba_settings.sqf" : {
        "add" : [
            "// cScripts Mission Settings",
            "force force cScripts_Settings_allowCustomInit = true;",
            "force force cScripts_Settings_allowCustomTagging = true;",
            "force force cScripts_Settings_allowInsigniaApplication = true;",
            "force force cScripts_Settings_curatorImmortality = false;",
            "force force cScripts_Settings_enable7cavZeusModules = true;",
            "force force cScripts_Settings_enableStartHint = false;",
            "force force cScripts_Settings_enforceEyewereBlacklist = true;",
            "force force cScripts_Settings_jumpSimulation = 1;",
            "force force cScripts_Settings_jumpSimulationGlasses = true;",
            "force force cScripts_Settings_jumpSimulationHat = true;",
            "force force cScripts_Settings_jumpSimulationNVG = true;",
            "force force cScripts_Settings_setAiSystemDifficulty = 0;",
            "force force cScripts_Settings_setCustomHintText = \"I have design this mission! Yey for me!\";",
            "force force cScripts_Settings_setCustomHintTopic = \"My custom Mission!\";",
            "force force cScripts_Settings_setMissionType = 2;",
            "force force cScripts_Settings_setPlayerRank = true;",
            "force force cScripts_Settings_setRadio = true;",
            "force force cScripts_Settings_setStartupDelay = 30;",
            "force force cScripts_Settings_showDiaryRecords = true;",
            "force force cScripts_Settings_useCustomSupplyInventory = false;",
            "force force cScripts_Settings_useCustomVehicleInventory = true;",
            "force force cScripts_Settings_useCustomVehicleSettings = true;"
        ]
    }
}
```
When cScripts is installed the `description.ext` and `init.sqf` will be overwritten to make sure custom scripts gets added include the script to the add section in the json file.
