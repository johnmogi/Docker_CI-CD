test pipeline rebuild with main commit

release

1. test merge with comment

git push --set-upstream origin test-merge
git checkout -b test

automation:
pipeline into artifact into release
-needs a connection to the deployment group 0. such as:

<!-- mkdir azagent;cd azagent;curl -fkSL -o vstsagent.tar.gz https://vstsagentpackage.azureedge.net/agent/2.204.0/vsts-agent-linux-x64-2.204.0.tar.gz;tar -zxvf vstsagent.tar.gz; if [ -x "$(command -v systemctl)" ]; then ./config.sh --deploymentgroup --deploymentgroupname "stage" --acceptteeeula --agent $HOSTNAME --url https://dev.azure.com/devjohnmogi/ --work _work --projectname 'weightapp' --runasservice; sudo ./svc.sh install; sudo ./svc.sh start; else ./config.sh --deploymentgroup --deploymentgroupname "stage" --acceptteeeula --agent $HOSTNAME --url https://dev.azure.com/devjohnmogi/ --work _work --projectname 'weightapp'; ./run.sh; fi -->

also it gets verified by PAT

new plan

1. make sure agent is restarting with oniline agent
2. install or transfer p-laybook once on the machine

wget https://vstsagentpackage.azureedge.net/agent/2.204.0/vsts-agent-linux-x64-2.204.0.tar.gz

crontab -e
@reboot /home/azureuser/run.sh


