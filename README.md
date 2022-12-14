# Jornada DevOps com AWS - Impulso

> Bootcamp gratuito promovido pela dio.

## Modulo Docker

**Desafio 02: Definição de um Cluster Swarm Local com Vagrant**

PASSO A PASSO:

1. Criar um Vagrantfile com as definições de 4 máquinas virtuais. Sendo uma máquina com o nome de master e as outras com os nomes de node01, node02 e node03; ✅
2. Cada máquina virtual deverá ter um IP fixo; ✅
3. Todas as MV deverão possuir o Docker pré-instalado; ✅
4. A máquina com o nome de master deverá ser o nó manager do cluster. ✅
5. As demais máquinas deverão ser incluídas no cluster Swarm como Workers. ✅

**Comentários:**

- Dada as limitações de hardware da minha máquina só foi possível subir 2 das 4 máquias virtuais solicitadas no desafio.
- Fiz algumas pequenas alterações no `Vagrantfile`, como uso de memória e cpu, para que as máquinas virtuais pudessem ser criadas no SO Windows da minha máquina física.
- Além dos passos pedidos acima, criei o script `create-container.sh` onde realiza a criação de um container rodando a imagem do Apache no nó de trabalho.

### Info

> Requisitos para execução dos scripts.

Necessária à instalação da **[Virtual Box](https://www.virtualbox.org/)** e **[Vagrant](https://www.vagrantup.com/)**.

- Vagrant é uma ferramenta para automatizar a criação de múltiplas máquinas virtual, utilizando de ferramentas de virtualização já conhecidas, como a Virtual Box, em uso nesse caso.

```ssh
# Para subir as máquias virtuais
$ vagrant up

# Alternar entre nós
$ vagrant ssh nome_no

# Apagar máquinas virtuais
$ vagrant destroy
```

**Para acessar o servidor Apache:**

- Acesse o ip no navegador: `10.0.18.11:80`
