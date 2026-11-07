# SkyWays Logistics --- Research Log

> **Purpose:** Maintain an evidence trail for the discovery phase of the
> SkyWays Logistics capstone.
>
> **Status:** Initial log. This file records only facts checked so far.
> Add a new row whenever a source, dataset, query, or experiment
> contributes to a project decision. Do not record assumptions as
> verified findings.

## Research log

  ---------------------------------------------------------------------------------------------------------------------------------------------
  Date          Source (title / file)                       Type          What it told me       Verification: how was it  Where it informs the
                                                                                                checked?                  project
  ------------- ------------------------------------------- ------------- --------------------- ------------------------- ---------------------
  07-Nov-2026   `SkyWays_Guided_Capstone_Brief_v1.0.pdf`,   Capstone      The truck journey is  Read the relevant page in Domain understanding;
                Part B, page 7 --- "Follow one truck"       brief         described in six      the supplied brief. This  candidate pain
                                                                          stages: shipment      verifies what the brief   points; Five Whys
                                                                          planning; driver and  describes, not how        research.
                                                                          vehicle assignment;   frequently each issue     
                                                                          appointment booking;  occurs in the dataset.    
                                                                          travel; gate/yard                               
                                                                          check-in; and                                   
                                                                          dock/unloading.                                 

  07-Nov-2026   `SkyWays_Guided_Capstone_Brief_v1.0.pdf`,   Capstone      The brief identifies  Read the relevant page.   Stakeholder analysis;
                Part B, page 8 --- "Who hurts, and how"     brief         five stakeholder      Impact statements are     problem statement;
                                                                          groups: driver,       scenario context until    PRD-lite.
                                                                          dispatcher/carrier,   independently measured.   
                                                                          operations                                      
                                                                          coordinator,                                    
                                                                          warehouse planner,                              
                                                                          and                                             
                                                                          consignee/customer.                             

  07-Nov-2026   `SkyWays_Guided_Capstone_Brief_v1.0.pdf`,   Capstone      Shipment,             Read the relevant page    Data exploration;
                Part B, page 9 --- "Where the truth lives"  brief         driver-message/ETA,   and noted the named       identify tables
                                                                          warehouse scheduling, systems and tables.       needed to investigate
                                                                          gate check-in, and                              an exception.
                                                                          confirmation                                    
                                                                          information is                                  
                                                                          distributed across                              
                                                                          different systems.                              

  07-Nov-2026   `SkyWays_Guided_Capstone_Brief_v1.0.pdf`,   Capstone      The brief traces one  Read the worked example.  Plan SQL exploration;
                Part B, page 11 --- "One message, traced"   brief /       driver message across It is not a frequency     understand
                                                            example trace operational records   estimate for all          message-to-shipment
                                                                          and says multiple     shipments.                and ETA traceability.
                                                                          data sources are                                
                                                                          needed before a                                 
                                                                          reliable response can                           
                                                                          be given.                                       

  07-Nov-2026   `SkyWays_Guided_Capstone_Brief_v1.0.pdf`,   Capstone      The brief provides    Read the examples. They   Generate candidate
                Part C, page 13 --- "Five Whys worked"      brief /       example root-cause    are candidate             problems for
                                                            worked        chains for            explanations from the     investigation.
                                                            examples      double-booking and    brief, not conclusions    
                                                                          unloading-duration    independently established 
                                                                          problems.             by this project.          

  07-Nov-2026   `SkyWays_Guided_Capstone_Brief_v1.0.pdf`,   Capstone      The brief gives an    Read the example          Scope selection;
                Part D, page 18 --- "PRD-lite in one page"  brief / scope example Agentic AI    PRD-lite. This is not a   avoid committing
                                                            example       scope focused on      decision that this        before discovery.
                                                                          converting a          project has selected that 
                                                                          free-text delay       solution.                 
                                                                          message into a                                  
                                                                          feasible held slot;                             
                                                                          it excludes                                     
                                                                          facility-wide                                   
                                                                          rescheduling from                               
                                                                          that example's scope.                           

  07-Nov-2026   `01_discover/discovery_prompts.md`          Starter-kit   The guide proposes    Inspected the supplied    Discovery plan and
                                                            research      research on warehouse Markdown file. Prompts    research questions.
                                                            guide         operations,           are research              
                                                                          root-cause            instructions, not         
                                                                          hypotheses, the       findings.                 
                                                                          difference between                              
                                                                          showing and reserving                           
                                                                          a slot, data                                    
                                                                          limitations, and                                
                                                                          design review. It                               
                                                                          also suggests a                                 
                                                                          vendor scan, paper                              
                                                                          skim, data probes,                              
                                                                          and review of                                   
                                                                          labelled driver                                 
                                                                          messages.                                       

  07-Nov-2026   `01_discover/five_whys_worksheet.md`        Starter-kit   The worksheet asks    Inspected the supplied    Root-cause analysis
                                                            worksheet     for one pain point    Markdown file.            deliverables.
                                                                          per analysis, five                              
                                                                          evidence-backed "why"                           
                                                                          levels, a                                       
                                                                          one-sentence root                               
                                                                          cause, and a decision                           
                                                                          for each level:                                 
                                                                          solve, mitigate,                                
                                                                          measure, or out of                              
                                                                          scope. It recommends                            
                                                                          investigating                                   
                                                                          multiple pain points.                           

  07-Nov-2026   `01_discover/pain_point_depth_matrix.md`    Starter-kit   The matrix scores     Inspected the supplied    Compare and select
                                                            scoring       candidate pain points Markdown file and scoring the capstone problem
                                                            framework     on frequency, cost,   guide. No candidate has   after data
                                                                          evidence, two-week    been scored yet.          investigation.
                                                                          solvability, and                                
                                                                          depth of root-cause                             
                                                                          evidence, each from                             
                                                                          1--5.                                           

  07-Nov-2026   `01_discover/research_log.md` (starter      Starter-kit   The template asks for Inspected the supplied    This research log.
                template)                                   template      date, source, source  Markdown file.            
                                                                          type, one-sentence                              
                                                                          finding, verification                           
                                                                          method, and where the                           
                                                                          finding is used in                              
                                                                          the build.                                      

  07-Nov-2026   `00_setup/setup_check.py` and local         Environment   The setup script      Ran                       Environment
                terminal output                             check         reported that Python  `python setup_check.py`   readiness. The
                                                                          3.10+, core packages, from the starter kit's    missing OpenRouter
                                                                          ML packages, Agentic  `00_setup` directory and  key matters only if
                                                                          packages, the SQLite  reviewed the terminal     the chosen
                                                                          database, 21 shipment output shared in this     implementation uses
                                                                          rows, four specified  conversation.             that configuration.
                                                                          views, and the                                  
                                                                          concurrency index                               
                                                                          passed. The                                     
                                                                          OpenRouter API-key                              
                                                                          check failed.                                   
  ---------------------------------------------------------------------------------------------------------------------------------------------

## Open questions --- not yet verified

1.  How many shipments have one or more ETA updates?
2.  How often do multiple trucks experience delays at the same facility
    during overlapping time windows?
3.  How often does a delay make an existing appointment infeasible?
4.  How many slot conflicts or double-booking attempts can be
    identified?
5.  How often are docks blocked, closed, or otherwise unavailable?
6.  How variable are unloading durations, and do overruns affect later
    appointments?
7.  Which operational problem has the strongest evidence and is feasible
    to address within the capstone timeline?

## Data probes to add

For every database investigation, record the exact question, SQL query
or notebook cell, row count and result, tables and columns used,
limitations, and the conclusion supported (including what it does not
prove).

## Research discipline

-   Separate facts from assumptions. Mark unverified explanations as
    `[assumption]`.
-   Do not infer frequency, cost, or causation from a single example.
-   Record the source and verification method for every important claim.
-   Keep negative or inconclusive findings; they are useful evidence
    too.
-   Update the PRD-lite and Five Whys only after the relevant evidence
    has been checked.
-   Do not claim that a solution improves performance until a baseline
    and repeatable evaluation support that claim.

## Current discovery status

-   [x] Read the initial capstone context and discovery templates.
-   [x] Run the starter-kit setup check.
-   [ ] Explore the supplied database and data dictionary.
-   [ ] Read and analyse the labelled driver messages.
-   [ ] Run data probes for candidate operational problems.
-   [ ] Complete multiple Five Whys analyses.
-   [ ] Score candidate pain points in the depth matrix.
-   [ ] Select and document one evidence-backed problem.
