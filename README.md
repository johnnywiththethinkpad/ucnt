# ucNT — User Control NT
ucNT is a proposed open-source Linux utility designed to provide an independent verification layer for Windows .exe files before they run through Wine, Proton, Bottles, or other compatible execution backends. The goal is to give users more information and control over the software they choose to run, without replacing the tools they already use.
ucNT is not intended to replace Wine, Proton, Bottles, or antivirus software. It cannot guarantee that an executable is harmless or eliminate every security risk but its purpose is to provide an additional verification and decision-support layer before execution.

## Architecture
* **The Input:** Windows executable (.exe) -> User double-clicks a file or selects “Verify with ucNT”.
* **ucNT Inspection Engine:** Computes SHA-256, reads PE metadata, checks digital signatures, publisher info, and file identity.
* **UCDE (User Control Decision Engine):** Evaluates evidence, resolves conflicts, records uncertainty, and produces a recommendation.

### Three Outcomes
1. **Recommended to run:** Evidence supports the file's claimed identity.
2. **Unable to recommend:** Evidence is insufficient or inconclusive.
3. **Not recommended to run:** Evidence conflicts with the claimed identity or indicates a meaningful concern.

## Pronunciation
Pronunciation: *U-C-N-T* spelled out letter-by-letter. Please do not mash it into one syllable, I know what it sounds like.

## Project Status
ucNT is currently in architectural design. Development and initial logic planning are underway. 

## License
ucNT is licensed under the [MIT License](LICENSE).
