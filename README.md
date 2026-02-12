# Migrate Changes Using Retrieved Update Sets

## Overview
This repository demonstrates the process of migrating configuration changes between ServiceNow instances using Update Sets. The focus is on retrieving an update set from an XML file, previewing platform changes for potential conflicts, committing the update set, and validating that configuration updates were successfully applied.

This project simulates how a ServiceNow administrator migrates configuration changes from one environment to another using the update set lifecycle.

## Use Case
An administrator needs to move configuration changes captured in an update set from one instance to another. The update set has been exported as an XML file and must be retrieved, reviewed, and committed to apply the changes to the target environment.

This project simulates how ServiceNow manages configuration migration using retrieved update sets, preview validation, and commit actions to safely apply platform changes.

## Features
- Retrieval of update sets from XML files
- Preview validation prior to commit
- Commit process for applying configuration changes
- Update set state management
- Verification of applied platform changes
- Controlled configuration migration workflow

## Technologies Used
- ServiceNow Platform
- Update Sets
- Retrieved Update Sets
- XML Import
- Preview Update Set
- Commit Update Set
- Problem Management

## Implementation Walkthrough

### Objective
Retrieve an exported update set, preview platform changes, commit the update set, and verify that configuration updates were successfully applied to the instance.

### Step 1: Verify Current State of the Problem Form
The Problem form was reviewed to confirm the Manufacturer field was not currently displayed.

A new Problem record was opened to validate the existing form layout prior to importing any changes.

This established a baseline state before migration.
S
### Step 2: Navigate to Retrieved Update Sets
Navigation was performed to **All > System Update Sets > Retrieved Update Sets** to prepare for importing the update set file.

This section manages update sets retrieved from external sources.

### Step 3: Import Update Set from XML
From the Related Links section, **Import Update Set from XML** was selected.

The XML file named **prb_manufacturer_update_set_25d31c7e9…xml** was chosen and uploaded.

Upon upload, the update set titled **Add Manufacturer to PRB Form (prb_manufacturer_update_set)** was created with a state of **Loaded**.

This confirmed the update set was successfully retrieved into the instance.

<img width="1907" height="261" alt="Screen Shot 2026-02-11 at 8 12 21 PM" src="https://github.com/user-attachments/assets/f18b5b5d-bb20-42a3-a940-58a35a7d3275" />

### Step 4: Review Customer Updates
The update set record was opened and the Customer Updates related list was reviewed.

This confirmed that the update set contained configuration changes related to the Problem form.

### Step 5: Preview the Update Set
The **Preview Update Set** action was selected.

The preview process compared the retrieved update set to the current local instance configuration to detect potential conflicts.

The preview completed successfully.

This validated that the update set could be committed without errors.

<img width="1907" height="261" alt="Screen Shot 2026-02-11 at 8 14 18 PM" src="https://github.com/user-attachments/assets/79b23e63-d54d-4215-9f52-1a3eafb303be" />

### Step 6: Commit the Update Set
The **Commit Update Set** action was selected to apply the configuration changes.

The commit process executed and reached 100 percent completion.

Committing applied all update records to the local instance and generated a committed update set record.

This finalized the migration of configuration changes.

<img width="1907" height="261" alt="Screen Shot 2026-02-11 at 8 14 43 PM" src="https://github.com/user-attachments/assets/a41f3248-1157-4e11-ab1d-5f9fc0631fb1" />

### Step 7: Verify Update Set State
Navigation returned to **All > System Update Sets > Retrieved Update Sets**.

The update set **Add Manufacturer to PRB Form** was confirmed to have a state of **Committed**.

This validated successful application of the update set.

<img width="1907" height="181" alt="Screen Shot 2026-02-11 at 8 17 14 PM" src="https://github.com/user-attachments/assets/9f171296-a178-4ae6-8c83-c7d624331448" />

## Validation and Testing

### Step 8: Verify Form Changes
A new Problem record was opened.

Under the Assigned to field, the **Manufacturer** field was verified to be present on the form.

This confirmed that the update set successfully modified the Problem form layout.

<img width="1907" height="419" alt="Screen Shot 2026-02-11 at 8 18 08 PM" src="https://github.com/user-attachments/assets/f471c1fc-451a-4f14-ad52-a183c62bc8cb" />

## Lessons Learned
- Update Sets provide a controlled method for migrating configuration changes
- Previewing an update set helps detect conflicts before applying changes
- Committing an update set applies all included configuration updates
- Retrieved Update Sets allow migration from XML exports
- Form layout changes can be safely moved between environments using update sets
