# **Desafio: Provisionamento Vagrant Shell Script Nginx**

<div>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vagrant/vagrant-original.svg" height="30" alt="vagrant logo" />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="30" alt="html5 logo" />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nginx/nginx-original.svg" height="30" alt="nginx logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bash/bash-original.svg" height="30" alt="bash logo" />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/ubuntu/ubuntu-plain.svg" height="30" alt="ubuntu logo" />
  
</div>

---

## **Sobre o Projeto**
Este projeto tem como objetivo automatizar a configuração de uma máquina virtual utilizando Vagrant com o sistema operacional Ubuntu 20.04 e provisioná-la para hospedar um site com Nginx. Toda a configuração é realizada através de um script de provisionamento (shell script), garantindo uma infraestrutura padronizada e escalável.

---

## **Pré-requisitos**
Antes de iniciar, certifique-se de ter instalado:
- [Vagrant](https://www.vagrantup.com/downloads)
- [VirtualBox](https://www.virtualbox.org/)
- Git Bash (para usuários Windows) ou Terminal no Linux/macOS

---

## **Instruções para Execução**
### 1. Clonar o Repositório
```bash
git clone https://github.com/williampaludo/vagrant-shell-script-nginx.git
cd vagrant-shell-script-nginx
```

### 2. Iniciar a Máquina Virtual
```bash
vagrant up
```
O comando acima criará e configurará automaticamente a máquina virtual, instalando o Nginx e configurando o ambiente.

### 3. Acessar a Máquina Virtual
```bash
vagrant ssh
```

---

## **Provisionamento Automático**
O script `provision.sh` realiza as seguintes configurações:
- Atualiza a lista de pacotes e instala o servidor Nginx.
- Configura a sincronização de pastas entre o host e a máquina virtual.
- Copia os arquivos do site para o diretório padrão do Nginx (`/var/www/html`).
- Reinicia o Nginx para aplicar as configurações.

---

## **Acessando o Site**
1. Após subir a VM, verifique o IP da máquina virtual executando o comando:
    ```bash
    ip a
    ```
2. Identifique o IP associado à interface de rede.
3. No navegador, acesse o site utilizando o IP identificado:
    ```
    http://<ip-da-vm>
    ```

---

## **Sincronização de Pastas**
A pasta compartilhada permite uma integração transparente entre o host e a máquina virtual:
- **Host:** `site`
- **VM:** `/var/www/html`

O arquivo html do site esta na pasta `site` rodando automaticamente no servido pelo Nginx.

---

## **Contribuições**
Contribuições são sempre bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

---

## **Links Importantes**
- [Documentação do Vagrant](https://www.vagrantup.com/docs)
- [Documentação do Nginx](https://nginx.org/en/docs/)
- [Repositório no GitHub](<url-do-repositorio>)

