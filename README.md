# RActuary Dialect

Over time and across regions insurance terms have evolved. Today, two insurance professional working in the same office will often use completely different terms to describe identical situations.  In different countries the discrepencies are far greater.  These discrepencies are usually not an issue for insurance professionals who can infer the intended meaning, but they are confusing to non insurance professionals.  

RActuary aims to reduce ambiguity in our work by using the **RActaury Dialect**.  The aim is to have the minimal number of definitions to make a complete insurance vocabulary.  The following definitions are based on those found in [BASIC RATEMAKING by Werner, Modlin, and Watson](https://www.casact.org/library/studynotes/Werner_Modlin_Ratemaking.pdf), with a few tweaks.

This will remain a living document until we are happy enough with the definitions to declare it version 1.  After version 1, new versions will be released less frequently.  Please open an issue or pull request if you have any suggestions. 

Words in [] are optional.  They can help to clarify communication, but are redundant.

1. Basic Insurance

- **insurer**: seller or provider of an insurance policy
- **insured**: purchaser or party covered by an insurance policy
- **insurance policy**: promise for insurer to indemnify the insured for the financial consequences of a covered event
- **premium**: the amount the insured pays for insurance coverage
- **exposure**: the basic unit of risk that underlies the insurance premium

2. Claims

- **claim**: the demand for indemnification by the insured
- **claimant**: the party making the claim for indemnification
- **accident date**: the date of the event that caused the loss
- **report date**: the date the insurer is made aware of the claim
- **reported claim**: a claim that has been reported to the insurer
- **origin [period]** the time period in which the claim is said to have originated for aggregation purposes.  Origin periods are more specifically defined as:
    - **accident [period]** the time period in which the accident occurred
    - **report [period]** the time period in which the claim was reported to the insurer
    - **policy [period]** the time period in which the policy was written

3. Loss

- **loss**: the amount paid or payable to the claimant under the terms of the insurance policy.  Loss is more specifically defined by the following terms (each of which are considered a loss):
    - **paid [loss]**: loss paid to claimant
    - **case [reserve]**: an estimate of the loss required to ultimately settle a particular claim
    - **reported [loss]**: $= paid + case$ Reported is often called incurred in practice, but we have chosen to use reported rather than incurred because incurred can mean several different things depending on who you ask
    - **IBNR [reserve]**: (**I**ncurred **B**ut **N**ot **R**eported) $= ultimate - reported$  IBNR can be further subdivided into:
        - **IBNER [reserve]**: (**I**ncurred **B**ut **N**ot **E**nough **R**eported) $= ultimate - reported$ on reported claims only
        - **IBNYR [reserve]**: (**I**ncurred **B**ut **N**ot **Y**et **R**eported) ultimate on unreported claims
    - **ultimate [loss]**: $= paid + case + IBNR$ total amount to settle claim. 

4. LAE (**L**oss **A**djustment **E**xpense)
