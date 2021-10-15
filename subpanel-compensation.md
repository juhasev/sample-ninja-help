### Sub Panel compensation

Enter the default compensation and revenue based on the LOI (Length Of Interview) for this sub panel. The compensation must be entered in **Reward Points**. CPI (Cost Per Incidence) is entered using **Reporting Currency**. The LOI is entered in minutes.

The compensation table starts with 0 and you can have as many tiers as you like. The system determines correct compensation automatically when you setup new projects. Let's imagine you have defined your compensation table as:

- A) LOI  0 min Reward points (completed)  100 CPI: $1.50 
- B) LOI  5 min Reward points (completed)  200 CPI: $3.00  
- C) LOI 10 min Reward points (completed)  300 CPI: $4.00  
- D) LOI 15 min Reward points (completed)  400 CPI: $5.00 

If project's LOI is set to 12 minutes compensation tier C is used. 
If project's LOI is over 15 the last tier is always used.

If you enter **CPI** or total **Project cost** in **Project Settings** Sample Ninja will automaticlly calculate and apply the correct CPI based on the LOI.

> You cannot edit the 0 LOI on the first tier, but you are free to setup as many LOI tiers as you like.

> **TIP** If you reward completes only you can toggle on **Rewards completes only** to simplify the compensation table.

