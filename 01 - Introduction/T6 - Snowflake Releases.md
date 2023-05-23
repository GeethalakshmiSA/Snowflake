# Snowflake Releases

* Users experience no downtime or disruption of service
* Release Types - **WEEKLY** (2 planned/scheduled release)
    1. Full Release - Has new features, feature enhancements/updates, fixes, behavior changes 
        *(Happens on any day of week except Friday)*
    2. Patch Release - Includes only fixes
       *(Happens after the Full Release)*
 * Behavior changes - **MONTHLY**
    - Happens each month except November & December
    - Selects 3rd and 4th weekly release for behavior changes
    - Behavior changes means any change to existing behavior that returns from before and may impact customer workloads
    - Provided in Bundle (YYYY-NN): where Y is year and N is ordinal number of release within a year
    - Example: 2022-06 (6th behavior change bundle in 2022)
    - Bundle Lifecycle:
        - Testing Period (1st month): Disabled by default
        - Opt-out Period (2nd month): Enabled by default
        - After opt-out period: Generally enabled
* Pre-release Testing/Validation
    - Release quality is Top Priority
    - Before each release deployment undergoes,
        - Regular build testing
        - Continuous workload and performance testing
    - Before any customer accounts move to release,
        - Full round of regression testing in internal accounts
        - Simulating execution of select impacted workload
* Staged Release Process
    - Before moving customers to release or full release deployment,
        - Early (DAY-1) => Stage 1 which is designated to Enterprise and above
        - Regular (DAY 1 or 2) => Stage 2 is for Standard accounts
        - Final (DAY 2) => For Enterprise and above

### Points to Note

*  Staged Approach => Then its Full Release and not the Patch Release
*  If issues encountered between/at release, then release is rolled back & completed within 24-48 hours
*  Early Access to full releases
    - To designate early access to account then contact Snowflake
    - Not recommended for all organizations
    - Recommended only for organization desired to add their production accounts to not get affected with full release
