transcript_file: the filename of the corresponding transcript
# characteristics
phd_attained: whether the participant has PhD [0=no|1=yes]
stroop_experience: whether the participant has experience with running stroop experiments [0=no|1=yes]
software_knowledge: the software typically used, as reported by the participant [string, separated by \\ ]
stat_knowledge: self assessed statistical knowledge [numeric, 0-10]
confidence_undetected: rating of confidence from participant for going undetected [numeric, 0-10]
days_fab: number of days across which participant fabricated data, not full days of data fabrication [count]
time_spent: estimate by participant of time spent [in hours]
perceived_effort: estimated effort on a Likert scale [1-7; "no effort at all"-"a lot of effort"]
runs: number of mean-sd combinations used before stopping data fabrication [count; if multiple values given, arithmetic mean of those]
miss_important: whether participant mentioned missing something important during the interview [0=no|1=yes]
# data fabrication characteristics for QCA
preparation: whether the participant made preparations before starting data fabrication (e.g., read on previously detected cases; [0=no|1=yes])
rng: whether the participant used a random number generator (e.g., simulate data, add noise; [0=no|1=yes])
real_stroop: whether the participant used real stroop data in the fabrication process [0=no|1=yes; does not include looking at literature]
duplicate_transform: whether the participant exactly duplicated data or used a transformation (i.e., duplication by formula, excluding noise addition because it falls under `rng`; [0=no|1=yes])
detect_check: whether the participant checked the fabricated data for detectability themselves using some empirical indicator [0=no|1=yes]
notes: some notes on the coding process [string; optional]
# outcomes
