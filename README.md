<div align="center"> 

# EasyEASM

EasyEASM repository for [Black Hat Arsenal 2023](https://www.blackhat.com/us-23/arsenal/schedule/index.html#easy-easm---the-zero-dollar-attack-surface-management-tool-33645) and [Recon Village @ DEF CON 2023](https://reconvillage.org/recon-village-talks-2023-defcon-31/).

</div>

## Description

Easy EASM is just that... the easiest to set-up tool to give your organization visibility into its external facing assets.

The industry is dominated by $30k vendors selling "Attack Surface Management," but OG bug bounty hunters and red teamers know the truth. External ASM was born out of the bug bounty scene. Most of these $30k vendors use this open-source tooling on the backend.

With ten lines of setup or less, using open source tools, and one button deployment, Easy EASM will give your organization a complete view of your online assets. Easy EASM scans you daily and alerts you via Slack or Discord on newly found assets! Easy EASM also spits out an Excel skeleton for a Risk Register or Asset Database! This isn't rocket science.. but it's USEFUL. Don't get scammed. Grab Easy EASM and feel confident you know what's facing attackers on the internet.

## Installation

```sh
go install github.com/g0ldencybersec/EasyEASM/easyeasm@latest
```

## Example Config file

The tool expects a configuration file named `config.yml` to be in the directory you are running from.

Here is example of this yaml file:

```yaml
# EasyEASM configurations
runConfig:
  domains:  # List root domains here.
    - example.com
    - mydomain.com
  slack: https://hooks.slack.com/services/DUMMYDATA/DUMMYDATA/RANDOM # Slack webhook url for Slack notifications.
  discord: https://discord.com/api/webhooks/DUMMYURL/Dasdfsdf # Discord webhook for Discord notifications.
  runType: fast   # Set to either fast (passive enum) or complete (active enumeration).
  activeWordList: subdomainWordlist.txt
  activeThreads: 100
```

## Usage

To run the tool, fill out the config file: `config.yml`. Then, run the `easyeasm` module:

```sh
./easyeasm
```

After the run is complete, you should see the output CSV (`EasyEASM.csv`) in the run directory. This CSV can be added to your asset database and risk register!

## Warranty

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) for details.

## Contact

- Gunnar Andrews @ 
- Olivia Gallucci @ olivia[@]oliviagallucci.com
- Jason Haddix @ 
