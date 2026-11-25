# Problem Set 5: Right 93% of the Time

## Recommendation to the Head of Risk

I suggest postponing the signing of the supplier contract. The accuracy rate reported by this supplier is 93%. Approving all applications yielded an accuracy rate of 93.47% on the simulation test set, and all 196 cases of default were missed.

I suggest testing the real loan data using the LASSO model and setting the rejection threshold at 0.126. In the simulation test set, this threshold successfully identified 88 out of 196 default cases and wrongly rejected 283 applicants who did not default. I assume that each missed default will result in a 60% loss of principal and that each incorrect rejection will cost 8% of principal in lost interest margin and $200 in lost goodwill. Based on these assumptions, compared to approving all applications, this threshold saved approximately 837202 dollars on the simulation test set. Calibration checks support the retention of the original LASSO probabilities and the 0.126 threshold in this analysis.

If the supplier's model uses a pre-set threshold on an independent set of recent loan applications and costs less than approving all applications, I will reconsider whether to sign the contract.
