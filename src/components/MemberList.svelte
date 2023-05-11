<script>
    import Accordion from "./Accordion.svelte";
    let names = [
        "Marco António Alves Almeida",
        "Daniel Alexandre Martins da Silva",
        "Adalberto Júnior Trindade Vaz do Rosário",
        "Maria Julia Nunes",
        "João Vitor da Rosa",
        "Ana Lídia da Mota",
        "João Guilherme da Paz",
        "Luis Gustavo Azevedo",
        "Gustavo Henrique Teixeira",
        "Maria Clara Barros",
        "Pedro Lucas da Rosa",
        "João Miguel da Rocha",
        "Vitor Gabriel Nascimento",
        "Ana Laura Barros",
        "Alexandre Tomás Rodrigues",
        "Bernardo Gonçalves",
        "Diogo Branco Silva",
        "Bruno Ferreira Gomes",
    ];
</script>

<main>
    <div class="shadow-none p-3 m-3 bg-light rounded">
        <h2 align="center">Lista de Membros</h2>
        <div class="accordion" id="accordionExample">
            {#each names as name, index}
                <Accordion {index} {name} />
            {/each}
        </div>
    </div>
</main>
