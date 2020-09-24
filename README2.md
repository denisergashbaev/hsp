To run assymetric self-play (not HSP!) in MazeBase environment, one needs the following launch config inside of the `launch.json` (notice arguments `--sp, --sp_extra_action, --sp_asym`)

```json
{
    "name": "Python: main.py --sp --env_name sp_goal --nactions 5 --max_steps 500 --plot --sp_extra_action --sp_asym --sp_test_rate 0.01 --sp_mode repeat --sp_state_thres 0.2",
    "type": "python",
    "request": "launch",
    "program": "${workspaceFolder}/hsp/main.py",
    "args": [
        "--seed", "0",
        "--nthreads", "1",
        "--sp", 
        "--env_name", "sp_goal", 
        "--nactions", "5", 
        "--max_steps",  "500", 
        "--sp_extra_action",
        "--sp_asym",
        "--sp_test_rate", "0.01", 
        "--sp_mode", "repeat", 
        "--sp_state_thres", "0.2", 
        "--plot"
    ],
    "console": "integratedTerminal"
}
```

The programming flow starts from `main.py` 