#create virtual env
pip install qsharp

#GET .NET Core SDK
wget https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb

sudo apt-get update;   sudo apt-get install -y apt-transport-https &&   sudo apt-get update &&   sudo apt-get install -y dotnet-sdk-3.1

#Install IQSharp
dotnet tool install -g Microdoft.Quantum.IQSharp

#This could return an error
dotnet iqsharp install
#so I went to
cd ~/.dotnet/tools/
~/.dotnet/tools/dotnet-iqsharp install --user --path-to-tool="~/.dotnet/tools/dotnet-iqsharp"

#Then installed QDK extension for VS Code: Microsoft Quantum Development Kit for Visual Studio Code

#Created the hello_world test on
cd q-test

python hello_world.py

#Output: Hello from quantum world!

