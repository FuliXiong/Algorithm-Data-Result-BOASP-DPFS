# BOASP-DPFS Data and Results Repository

This repository contains the experimental data and computational results for the paper:

**"Bilevel order acceptance and scheduling in distributed permutation flow shop systems"**

Authors: Fuli Xiong, Chengfei Xiang

BOASP-DPFS/
├── Data/
│   ├── test_instances/           # Full test instance set (974 instances)
│   │
│   └── sampled_instances/        # Sampled instances for ablation study (144 instances)                       
│
└── Result/
    ├── Small/                    # Small-scale instance results (J ≤ 25)
    │   ├── HPR-LBBD-small.csv
    │   ├── HPR-BCH-small.csv
    │   ├── RHPR-LBBD-small.csv
    │   ├── RHPR-BCH-small.csv
    │   ├── MIBS-small.csv
    │   └── OASP-DPFS-small.csv   # Single-level baseline
    │
    ├── Large/                    # Large-scale instance results (J ≥ 30)
    │   ├── HPR-LBBD-big.csv
    │   ├── HPR-BCH-big.csv
    │   ├── RHPR-LBBD-big.csv
    │   └── RHPR-BCH-big.csv
    │
    ├── sampled/                  # Ablation study results
    │   ├── RHPR-LBBD.csv
    │   ├── RHPR-no-2s.csv        
    │   ├── RHPR-no-alls.csv     
    │   ├── RHPR-no-cut1.csv     
    │   ├── RHPR-no-cut2.csv      
    │   └── RHPR-no-fix-ub.csv    
    │
    ├── Parameter tuning/         # Algorithm parameter tuning results
    │   ├── ga_tuning_results.csv     # GA
    │   ├── pso_tuning_results.csv    # PSO:
    │   ├── vns_tuning_results.csv    # VNS
    │   └── woa_tuning_result.csv     # WOA
    │
    └── Comparison with metaheuristics/  # Metaheuristic comparison results
        ├── RHPR-LBBD(300s).csv
        ├── GA.csv                
        ├── WOA.csv                
        ├── VNS.csv                
        └── PSO.csv               


Experimental Design

Experiment 1: Small-Scale Instance Comparison (Section 5.2)

**Data:** `Data/test_instances/` (J ∈ {5,10,15,20,25}, 540 instances)  
**Results:** `Result/Small/`  
Algorithms:HPR-LBBD,HPR-BCH,RHPR-LBBD ⭐,RHPR-BCH,MibS

Experiment 2: Large-Scale Instance Comparison (Section 5.3)
**Data:** `Data/test_instances/` (J ∈ {30,50,70}, 434 instances)  
**Results:** `Result/Large/`  
Algorithms:HPR-LBBD,HPR-BCH,RHPR-LBBD ⭐,RHPR-BCH

Experiment 3: Ablation Study (Section 5.4)
**Data:** `Data/sampled_instances/` (144 instances)  
**Results:** `Result/sampled/`  
Algorithms:RHPR-LBBD ⭐,RHPR-no-2s,RHPR-no-alls,RHPR-no-cut1,RHPR-no-cut2,RHPR-no-fix-ub

Experiment 4: Metaheuristic Comparison (Section 5.5)
**Data:** `Data/sampled_instances/` (144 instances)  
**Results:** `Result/Large/` (GA.csv, PSO.csv, WOA.csv, VNS.csv, RHPR-LBBD(300s).csv)  
Algorithms:,RHPR-LBBD(300s) ⭐,GA,PSO,WOA,VNS

Experiment 5: Managerial Implications (Section 5.6)
**Data:** `Data/test_instances/` (small-scale instances)  
**Results:** `Result/Small/OASP-DPFS-small.csv` & `Result/Small/RHPR-LBBD-small.csv`  
**Experiments:**
- Bilevel vs. single-level model comparison: BOASP-DPFS vs OASP-DPFS
- Performance analysis of RHPR-LBBD under different rejection cost levels

