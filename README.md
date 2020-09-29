# MARL-with-SQLoss

## Installation instructions:
- Use the following commands to setup the virtual-env with the required packages.
```
sudo apt-get install python3-pip
sudo pip3 install virtualenv 
virtualenv -p python3 venv
source venv/bin/activate
export LC_ALL=C.UTF-8
export LANG=C.UTF-8
pip3 install -r requirements.txt
```

- You can also refer to the file `requirements-freezed.txt` to obtain the exact version of a package used for our experiments if there is any installation issue.
- <ins>NOTE</ins>: The code is *NOT* compatible with python2. Please use python3.



## Execution Instructions
- After the environment setup is complete, you can run the `IPD with SQLoss` experiment shown in the paper using the command below:
```
python3 scripts/run_sqloss.py --exp_name=IPD --no-lola --no-exact --trials=1 --batch_size=200 --trace_length=200 --num_episodes=12000 --lr=1.0
```
- It would take approximately <ins>25 minutes</ins> to finish around 55 training epochs which should be enough time to get the results. It is also a hard stop based on the parameters above. If the code execution ends prematurely then consider increasing the `--num_episodes` param (200 episodes == 1 training epoch) to get the results.

## Logs
- Logs are generated in the folder `logs/` for all the experiments.
- Folder `paper_logs` contains the logs for the results in the paper

**Note:** this code is not tested on GPU, so there might be unexpected issues.

*Disclaimer:* This is a research code release that has not been tested beyond the use cases and experiments discussed in the original papers.

## Additional Resources
---

## Credits
We use the code backbone provided by Learning with opponent leanrning awareness (LOLA) for our experiments.
```
@inproceedings{foerster2018lola,
  title={Learning with opponent-learning awareness},
  author={Foerster, Jakob and Chen, Richard Y and Al-Shedivat, Maruan and Whiteson, Shimon and Abbeel, Pieter and Mordatch, Igor},
  booktitle={Proceedings of the 17th International Conference on Autonomous Agents and MultiAgent Systems},
  pages={122--130},
  year={2018},
  organization={International Foundation for Autonomous Agents and Multiagent Systems}
}
```

## License

MIT
