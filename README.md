### Fast Flow Framework - WDG Automation ###
**FFF-WDG**

FFF is a framework for fast RPA development and ease of use in mind.

It follow good pratices of each tool and also keep a good usability and consistency.

### Overview ###
1. **Init**
 + *LoadConfiguration* - Load config data from file and from assets.

2. **Get Data**
 + *Retrieve Data* - Extract base data to work with.
 
3. **Transaction**
 + *Transactions* - Core process automated should be placed here.
    + *Transaction State Machine* - State machine that will contain each step of the process creating a *checkpoint* between each step.
 + *Transitions*
    + *Next Transaction* - Select next transaction by incrementing intTransactionNumber.
    + *Exception* - Any exception (System exception or rule violation) that ocurre during process execution.
    + *End Prcocess* - No more transaction to process or a **Stop** was requested by Orchestrator.
 
4. **Error Handler**
 +  *Get Exception* - Default behaviour to handle exception.
 +  *Next Step* - Check whether it is necessary to continue with the current transaction or skip to the next one.

5. **End Process**
 +  *Final Steps* - Final steps of the process. Ex.: Send an e-mail, writing a log file, closing applications used, etc.

### How to Use ###

This framerwork work on WDG Automation 20.10.4.0 or newer.

Not ready for production.