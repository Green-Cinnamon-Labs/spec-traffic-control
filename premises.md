# Traffic Adaptive Control LAB — Technical Premises

---

## Premise Block — Example

### Premise ID: P-001  
**Statement**  
> The simulation engine must control time progression, not the numerical solver.

**Scope**  
> Applies to all model implementations.

**Condition of Validity**  
> Valid while fixed-step deterministic execution is required.

**Impact if False**  
> Loss of reproducibility and architectural coupling between solver and execution layer.

**Status**  
> Active | Under Review | Deprecated
