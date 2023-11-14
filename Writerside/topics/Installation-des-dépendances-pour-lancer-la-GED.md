# Installation des dépendances pour lancer la GED

**Connectez-vous en SSH au terminal de la VM**

## Installation des dépendances

```bash
sudo apt install apt-transport-https ca-certificates curl gnupg-agent software-properties-common git python2.7 npm -y
```

## Installation de Docker

```bash
sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg
```

<tabs>
    <tab title="Linux Mint">
        <code-block lang="bash">
echo \
"deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
"$(. /etc/os-release &amp;&amp; echo "$UBUNTU_CODENAME")" stable" | \
sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
        </code-block>
    </tab>
    <tab title="Ubuntu Server">
        <code-block lang="bash">
echo \
"deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
"$(. /etc/os-release &amp;&amp; echo "$VERSION_CODENAME")" stable" | \
sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
        </code-block>
    </tab>
</tabs>

```bash
sudo apt-get update
```

```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

## Ajouter les permissions pour utiliser docker sans sudo

```bash
sudo groupadd docker
sudo usermod -aG docker $USER
```