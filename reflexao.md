# Reflexão

## O que exatamente causou o conflito?

O conflito aconteceu porque eu (Thauany) e o Guilherme editamos a mesma linha do README.md, o título da primeira linha, cada um na sua máquina e sem dar `git pull` antes. Eu enviei minha alteração primeiro. Quando o Guilherme tentou dar `git push`, o Git recusou, porque o GitHub já tinha um commit que ele não tinha. Ao rodar `git pull`, o Git viu duas versões diferentes da mesma linha e não conseguiu decidir sozinho qual manter, então marcou o arquivo com `<<<<<<<`, `=======` e `>>>>>>>`.

## Como vocês decidiram qual versão manter?

Conversamos pelo WhatsApp e decidimos juntar os dois em um só: duo git thauany guilherme Easy. Depois o Guilherme apagou os marcadores de conflito no README.md, deixou só o título escolhido, e fez `git add`, `git commit` e `git push` com a mensagem "Resolve conflito no título do README".

## Se isso acontecesse num projeto real com várias pessoas mexendo no mesmo arquivo o tempo todo, o que vocês fariam diferente?

Daríamos `git pull` antes de começar a trabalhar e antes de cada `git push`, para sempre partir da versão mais recente. Faríamos commits pequenos e frequentes, para que cada conflito fosse pequeno e fácil de resolver. Também combinaríamos quem mexe em qual arquivo ou trecho, e usaríamos branches separadas por tarefa, com pull requests para revisar antes de juntar tudo na `main`.