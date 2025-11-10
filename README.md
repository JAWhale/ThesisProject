PSCAD .psout files: https://mqoutlook-my.sharepoint.com/:u:/g/personal/joshua_whale_students_mq_edu_au/EQhA4qlycTtJti3OepkR_GMBnpDnn5pDSwETh2I0Lg1n4w?e=JaPcIn
MATLAB Files: https://mqoutlook-my.sharepoint.com/:u:/g/personal/joshua_whale_students_mq_edu_au/EZAiEBHNBJREkhHk8RlvkKwB-9oIXIKXIcj6N0q16D8wyQ?e=6io6EG
**************************** MATLAB README ******************************************************

The MATLAB script PlotFromCSV inside the zipped matlabCode folder contains a suite of plotting and data import functions designed to visualize generator and grid behavior from structured Excel datasets. It supports time-domain and characteristic plots for active power, reactive power, voltage, frequency, and angle responses.

Function List and Usage Examples

1. 	plotActivePowerDeviation
• 	Plots active power deviation for Gen 1–3
• 	Example:
plotActivePowerDeviation(Base3SGSmall, BaseGFL1Small, 1);

3. 	plotReactivePowerDeviation
• 	Plots reactive power deviation for Gen 1–3
• 	Example:
plotReactivePowerDeviation(Base3SGSmall, BaseGFL1Small, 1);

4. 	plotFrequencyDeviation
• 	Plots frequency deviation for Gen 1–3 and average frequency
• 	Example:
plotFrequencyDeviation(Base3SGSmall, BaseGFL1Small, 1);

5. 	plotGeneratorBusesVoltageDeviation
• 	Plots voltage deviation for Gen 1–3
• 	Example:
plotGeneratorBusesVoltageDeviation(Base3SGSmall, BaseGFL1Small, 1);

6. 	plotActivePowerAngleCharacteristicGen2
• 	Plots P–δ characteristic and time-domain responses for Gen 2
• 	Example:
plotActivePowerAngleCharacteristicGen2(GFL13Smallvariants{:});

7. 	plotActivePowerFrequencyCharacteristicGen2
• 	Plots P–F characteristic and time-domain responses for Gen 2
• 	Example:
plotActivePowerFrequencyCharacteristicGen2(GFM13Smallvariants{:});

8. 	plotActivePowerVoltageCharacteristicGen2
• 	Plots V–Q characteristic and time-domain responses for Gen 2
• 	Example:
plotActivePowerVoltageCharacteristicGen2(BaseGFL1Large, IncGFL1Large, 1);

9. 	plotVoltageReactivePowerCharacteristicGen2
• 	Plots Q–V characteristic and time-domain responses for Gen 2
• 	Example:
plotVoltageReactivePowerCharacteristicGen2(Base3SGLarge, BaseGFM1Large, 1);

10. 	plotRocofTimeDomainResponse
• 	Placeholder for future implementation of ROCOF time-domain plots

11. 	importTablesFromExcel
• 	Imports all sheets from a specified Excel file as tables
• 	Example:
importTablesFromExcel("filepath.xlsx", 1);

11. 	importSelectedSheetsFromExcel
• 	Imports specified sheets from an Excel file
• 	Example:
importSelectedSheetsFromExcel("filepath.xlsx", "Sheet1", "Sheet2", 1);

Important Notes

• 	Legends in plots do not automatically update to reflect the names of your input datasets. They default to "Dataset 1", "Dataset 2", etc.
• 	For clearer interpretation, consider manually editing legend labels or modifying the functions to accept dataset names.

Data Import and Reload Workflow

1. 	Use  or  to load data from Excel files formatted like the provided examples.
2. 	Once imported, select the table in the MATLAB Workspace.
3. 	Save the table as a  file for faster reuse: save('MyDataset.mat', 'ImportedTableName');
4. 	Reload the table later with: load('MyDataset.mat');
This avoids repeated Excel imports and speeds up your workflow
