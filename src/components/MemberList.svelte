<script>
    import Accordion from "./Accordion.svelte";
    import SearchBar from "./SearchBar.svelte";
    export let names = [
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

    let filteredNames = names;

    let searchTerm = "";
    function handleSearch(value) {
        searchTerm = value.toLowerCase();
        filteredNames = names.filter((name) =>
            name.toLowerCase().includes(searchTerm)
        );
    }
</script>

<main>
    <div class="shadow-none p-3 m-3 bg-light rounded">
        <h2 align="center">Lista de Membros</h2>
        <SearchBar onSearch={handleSearch} />
        <div class="faq-list">
            {#each filteredNames as person, index}
                <div class="accordion" id="accordionExample">
                    <Accordion {index} name={person} />
                </div>
            {/each}
        </div>
    </div>
</main>
