<script>
    import Contact from "./Contact.svelte";
    var n = [1, 1, 1, 1, 1, 1, 1, 1, 1];
    var files;
    var fileCount = 0;
    $: if (files) {
        fileCount = files.length;
	}
    
    function openFileExplorer() {
        document.getElementById("file-input").click();
    }
    const chatNames = [
        "Marco Almeida",
        "Daniel Silva",
        "Adalberto Rosário",
        "Maria Nunes",
        "João Rosa",
        "Ana Mota",
        "João Paz",
        "Luis Azevedo",
        "Gustavo Teixeira",
    ];
    import { nameList } from "./MemberList.svelte";
</script>

<main>
    <div
        style="height: 100%; width: 75%; position: absolute; top: 0; left: 0;"
        class="p-3"
    >
        <div style="height: 100%" class="shadow-none p-3 bg-light rounded">
            <div style="height: 100%; overflow: auto">
                <!-- class= "hide-scrollbar" para esconder scrollbar -->
                <div id="top" class="card mb-3">
                    <div class="card-body">
                        <div class="row">
                            <div class="col-md-1">
                                <!-- This div will take up 10% of the left space -->
                                <div>
                                    <img
                                        src="static/default_avatar.png"
                                        style="width: 50px; heigth: 50px"
                                        class="m-1"
                                        alt="user"
                                    />
                                </div>
                            </div>
                            <div class="col-md-11">
                                <!-- The main content of the card-body goes here -->
                                <div class="mb-3">
                                    <textarea
                                        class="form-control"
                                        id="exampleFormControlTextarea1"
                                        rows="3"
                                        placeholder="Escreva algo..."
                                    />
                                </div>
                                <div
                                    class="d-flex justify-content-between align-items-center"
                                >
                                    <div class="d-flex">
                                        <button
                                            type="button"
                                            on:click={openFileExplorer}
                                            class="btn btn-link"
                                            ><i
                                                class="bi bi-image-fill"
                                            />
                                            {#if fileCount>0}
                                                {fileCount}
                                            {/if}
                                            </button
                                        >
                                        <input
                                            bind:files
                                            type="file"
                                            id="file-input"
                                            style="display: none"
                                            accept="image/png, image/jpeg, video/mp4 ,video/x-m4v, video/*"
                                            multiple
                                        />
                                        <button
                                            type="button"
                                            class="btn btn-link"
                                            ><i
                                                class="bi bi-emoji-smile"
                                            /></button
                                        >
                                        <button
                                            type="button"
                                            class="btn btn-link"
                                            ><svg
                                                xmlns="http://www.w3.org/2000/svg"
                                                class="svg-icon"
                                                style="width: 1em; height: 1em;vertical-align: middle;fill: currentColor;overflow: hidden; vertical-align: -3px;"
                                                viewBox="0 0 1024 1024"
                                                version="1.1"
                                                ><path
                                                    d="M128 938.666667V341.333333h170.666667v597.333334H128m298.666667 0V85.333333h170.666666v853.333334h-170.666666m298.666666 0v-341.333334h170.666667v341.333334h-170.666667z"
                                                    fill=""
                                                /><path
                                                    xmlns="http://www.w3.org/2000/svg"
                                                    d="M128 938.666667V341.333333h170.666667v597.333334H128m298.666667 0V85.333333h170.666666v853.333334h-170.666666m298.666666 0v-341.333334h170.666667v341.333334h-170.666667z"
                                                    fill=""
                                                /></svg
                                            ></button
                                        >
                                    </div>
                                    <button class="btn btn-primary"
                                        >Publicar</button
                                    >
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="p-3 mt-3 bg-body rounded" style="width: 100%">
                    <img
                        src="static/default_avatar.png"
                        style="width: 50px; heigth: 50px"
                        class="m-3"
                        alt="user"
                    />
                    <h5 style="display: inline" class="">Manel Escuteiro</h5>
                    <p class="m-3">
                        Grande dia!
                    </p>
                    <img
                        src="https://flordelis.escutismo.pt/wp-content/uploads/sites/2/2021/01/porque-contratar-uma-pessoa-que-tenha-sido-escuteira.jpg"
                        style="width: 100%"
                        alt="nerd"
                    />
                </div>
                <div class="p-3 mt-3 bg-body rounded" style="width: 100%">
                    <img
                        src="static/default_avatar.png"
                        style="width: 50px; heigth: 50px"
                        class="m-3"
                        alt="user"
                    />
                    <h5 style="display: inline" class="">João Escuteiro</h5>
                    <p class="m-3">
                        A melhor foto que tiramos há duas semanas!
                    </p>
                    <img
                        src="https://escutismo.pt/img/full/dirigentes_161122022331_lisboa.jpg"
                        style="width: 100%"
                        alt=""
                    />
                </div>
                <div class="p-3 mt-3 bg-body rounded" style="width: 100%">
                    <img
                        src="static/default_avatar.png"
                        style="width: 50px; heigth: 50px"
                        class="m-3"
                        alt="user"
                    />
                    <h5 style="display: inline" class="">Zé Escuteiro</h5>
                    <p class="m-3">
                        Foto de grupo de ontém!
                    </p>
                    <img
                        src="https://agencia.ecclesia.pt/portal/wp-content/uploads/2018/04/Escutismo.jpg"
                        style="width: 100%"
                        alt=""
                    />
                </div>
            </div>
        </div>
    </div>
    <div
        style="height: 100%; width: 25%; position: absolute; top: 0; right: 0;"
        class="p-3"
    >
        <div style="height: 100%" class="shadow-none p-3 bg-light rounded">
            <div
                style="height: 50%"
                class="shadow-none m-1 rounded"
            >
            <div class="mb-3" style="text-align: center">
                <h5><b>Contactos</b></h5>
            </div>
            <div style="height: 85%; overflow: auto">
                {#each nameList as chatName}
                    <Contact person={chatName} />
                {/each}
            </div>
            </div>
            <div
                style="height: 50%"
                class="shadow-none m-1 rounded"
            >
            <div class="mb-3" style="text-align: center">
                <h5><b>João Rosa</b></h5>
            </div>
            <div style="height: 85%; overflow: auto">
                <div>
                    <div class="mb-1 p-3 bg-body" style="width: 100%">
                    <p style="display: inline" class="">Vais a alguma atividade no próximo mês?</p>
                    </div>
                    <div class="mb-1 p-3 bg-body" style="width: 100%; text-align: right">
                    <p style="display: inline" class="">Acho que só vou a uma</p>
                    </div><div class="mb-1 p-3 bg-body" style="width: 100%">
                    <p style="display: inline" class="">Qual?</p>
                    </div><div class="mb-1 p-3 bg-body" style="width: 100%; text-align: right">
                    <p style="display: inline" class="">Dia 26</p>
                    </div><div class="mb-1 p-3 bg-body" style="width: 100%">
                    <p style="display: inline" class="">Vemo-nos lá então!!</p>
                    </div>
                    <textarea class="form-control" style="height: 20px" />
                    <button
                        class="form-control btn btn-primary"
                        style="height: 1%;">Enviar</button
                    >
                </div>
            </div>
            </div>
        </div>
    </div>
</main>

<style>
    .hide-scrollbar {
        overflow-y: scroll;
        /* set the height and width of the element as needed */
    }

    .hide-scrollbar::-webkit-scrollbar {
        display: none;
    }

    textarea {
        resize: none;
        height: auto;
        overflow-y: hidden;
    }

    textarea:active,
    textarea:focus {
        outline: none;
    }
</style>
