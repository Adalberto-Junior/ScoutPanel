<script context="module">
    const commonProperties = {
        address: "Morada",
        phoneNumber: "Telemovel/Telefone",
        email: "Endereço de Email",
        birthDate: "Data de nascimento",
        sex: "Masculino/Feminino/Outro",
        bio: "Uma biografia muito longa.",
        image: "static/default_avatar.png",
    };

    export const nameList = [
        Object.assign({}, commonProperties, {
            name: "Marco António Alves Almeida",
        }),
        Object.assign({}, commonProperties, {
            name: "Daniel Alexandre Martins da Silva",
        }),
        Object.assign({}, commonProperties, {
            name: "Adalberto Júnior Trindade Vaz do Rosário",
        }),
        Object.assign({}, commonProperties, {
            name: "Maria Julia Nunes",
        }),
        Object.assign({}, commonProperties, {
            name: "João Vitor da Rosa",
        }),
        Object.assign({}, commonProperties, {
            name: "Ana Lídia da Mota",
        }),
        Object.assign({}, commonProperties, {
            name: "João Guilherme da Paz",
        }),
        Object.assign({}, commonProperties, {
            name: "Luis Gustavo Azevedo",
        }),
        Object.assign({}, commonProperties, {
            name: "Gustavo Henrique Teixeira",
        }),
        Object.assign({}, commonProperties, {
            name: "Maria Clara Barros",
        }),
        Object.assign({}, commonProperties, {
            name: "Pedro Lucas da Rosa",
        }),
        Object.assign({}, commonProperties, {
            name: "João Miguel da Rocha",
        }),
        Object.assign({}, commonProperties, {
            name: "Vitor Gabriel Nascimento",
        }),
        Object.assign({}, commonProperties, {
            name: "Ana Laura Barros",
        }),
        Object.assign({}, commonProperties, {
            name: "Alexandre Tomás Rodrigues",
        }),
        Object.assign({}, commonProperties, {
            name: "Bernardo Gonçalves",
        }),
        Object.assign({}, commonProperties, {
            name: "Diogo Branco Silva",
        }),
        Object.assign({}, commonProperties, {
            name: "Bruno Ferreira Gomes",
        }),
    ];
</script>

<script>
    import NestedAccordion from "./NestedAccordion.svelte";
    import SearchBar from "./SearchBar.svelte";

    let filteredNames = nameList;

    function handleSearch(value) {
        let searchTerm = value.trim().toLowerCase();
        filteredNames = nameList.filter(({ name }) =>
            name
                .normalize("NFD")
                .replace(/[\u0300-\u036f]/g, "")
                .toLowerCase()
                .includes(searchTerm)
        );
    }
</script>

<main>
    <div class="shadow-none p-3 m-3 bg-light rounded">
        <h2 align="center">Lista de Membros</h2>
        <SearchBar onSearch={handleSearch} />
        <div class="faq-list">
            {#each filteredNames as person, index}
                <div class="m-1">
                    <NestedAccordion {index} {person} />
                </div>
            {/each}
        </div>
    </div>
</main>
