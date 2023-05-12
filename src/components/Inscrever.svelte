<script>
    import { admin_tab } from "../stores/stores.js";
    let _admin_tab;
    admin_tab.subscribe((value) => {
        _admin_tab = value;
    });

    let avatar, fileinput;
    import { nameList } from "./MemberList.svelte";
    let newMemberName = "";
    let newMemberAddress = "";
    let newMemberNumber = "";
    let newMemberEmail = "";
    let newMemberBirthdate = "";
    let newMemberSex = "";
    let newMemberBio = "";
    const onFileSelected = (e) => {
        let image = e.target.files[0];
        let reader = new FileReader();
        reader.readAsDataURL(image);
        reader.onload = (e) => {
            avatar = e.target.result;
        };
    };
    function signup() {
        if (!avatar) {
            avatar =
                "static/default_avatar.png";
        }
        nameList.push({
            name: newMemberName,
            address: newMemberAddress,
            phoneNumber: newMemberNumber,
            email: newMemberEmail,
            birthDate: newMemberBirthdate,
            sex: newMemberSex,
            bio: newMemberBio,
            image: avatar,
        });
    }
</script>

<main>
    <div class="shadow-none p-3 m-3 bg-light rounded">
        <h2 align="center">Formulário de inscrição</h2>
        <label for="nome" class="form-label m-1">Nome Completo</label>
        <input
            bind:value={newMemberName}
            type="text"
            class="form-control"
            id="nome"
        />
        <label for="morada" class="form-label m-1">Morada</label>
        <input
            bind:value={newMemberAddress}
            type="text"
            class="form-control"
            id="morada"
        />

        <label for="number" class="form-label m-1">Telemóvel/Telefone</label>
        <input
            bind:value={newMemberNumber}
            type="number"
            class="form-control"
            id="number"
        />

        <label for="date" class="form-label m-1">Data de nascimento</label>
        <input
            bind:value={newMemberBirthdate}
            type="date"
            class="form-control"
            id="date"
        />

        <label for="email" class="form-label m-1">Endereço de Email</label>
        <input
            bind:value={newMemberEmail}
            type="email"
            class="form-control"
            id="email"
            placeholder="name@example.com"
        />
        <label for="sexo" class="form-label m-1">Sexo</label>
        <select bind:value={newMemberSex} class="form-select" aria-label="Sexo">
            <option value="Feminino">Feminino</option>
            <option value="Masculino">Masculino</option>
            <option value="Outro">Outro</option>
        </select>

        <label for="aboutme" class="form-label m-1">Biografia</label>
        <textarea
            bind:value={newMemberBio}
            class="form-control"
            id="exampleFormControlTextarea1"
            rows="3"
        />
        <div id="app" class="m-1 p-3">
            {#if avatar}
                <img class="avatar" src={avatar} alt="d" />
            {:else}
                <img
                    class="avatar"
                    src="static/default_avatar.png"
                    alt="Default Avatar"
                />
            {/if}
            <input
                type="image"
                class="upload"
                src="static/camera.png"
                alt="Submeter imagem"
                on:click={() => {
                    fileinput.click();
                }}
            />
            Fotografia de Escuteiro
            <input
                style="display:none"
                type="file"
                accept=".jpg, .jpeg, .png"
                on:change={(e) => onFileSelected(e)}
                bind:this={fileinput}
            />
        </div>
        <!-- Button trigger modal -->
        <button
            on:click={signup}
            type="button"
            class="btn btn-primary"
            data-bs-toggle="modal"
            data-bs-target="#exampleModal"
        >
            Inscrever
        </button>

        <!-- Modal -->
        <div
            class="modal fade"
            id="exampleModal"
            tabindex="-1"
            aria-labelledby="exampleModalLabel"
            aria-hidden="true"
        >
            <div class="modal-dialog">
                <div class="modal-content">
                    <div class="modal-header">
                        <h1 class="modal-title fs-5" id="exampleModalLabel">
                            Sucesso!
                        </h1>
                        <button
                            type="button"
                            class="btn-close"
                            data-bs-dismiss="modal"
                            aria-label="Close"
                        />
                    </div>
                    <div class="modal-body">Membro inscrito com sucesso!</div>
                    <div class="modal-footer">
                        <button
                            type="button"
                            data-bs-dismiss="modal"
                            class="btn btn-primary"
                            on:click={() => admin_tab.update(() => "lista")}
                            >Ver lista de membros</button
                        >
                        <!-- TODO: Meter este botao a dar redirect para a lista de membros -->
                    </div>
                </div>
            </div>
        </div>
    </div>
</main>

<style>
    #app {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-flow: column;
    }

    .upload {
        display: flex;
        height: 50px;
        width: 50px;
        cursor: pointer;
    }
    .avatar {
        display: flex;
        height: 200px;
        width: 200px;
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
