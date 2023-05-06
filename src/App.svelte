<script>
    import Home from "./components/Home.svelte";
    import Admin from "./components/Admin.svelte";
    
    var main_tab = "admin"
</script>

<main>
    <div style="height: 100%; width: 20%; position: absolute; top: 0; left: 0;">
        <div class="shadow-none p-3 m-3 bg-light rounded"><a href="#" class="nav-link" style="display: block" on:click={()=>main_tab="home"}>ScoutPanel</a></div>
        <div class="shadow-none p-3 m-3 bg-light rounded"><a href="#" class="nav-link" style="display: block" on:click={()=>main_tab="perfil"}>Perfil</a></div>
        <div class="shadow-none p-3 m-3 bg-light rounded"><a href="#" class="nav-link" style="display: block" on:click={()=>main_tab="notificacoes"}>Notificações</a></div>
        <div class="shadow-none p-3 m-3 bg-light rounded"><a href="#" class="nav-link" style="display: block" on:click={()=>main_tab="admin"}>Admin</a></div>
        <div class="shadow-none p-3 m-3 bg-light rounded"><a href="#" class="nav-link" style="display: block" on:click={()=>main_tab="definicoes"}>Definições</a></div>
        <div class="shadow-none p-3 m-3 bg-light rounded"><a href="#" class="nav-link" style="display: block" on:click={()=>main_tab="pagamentos"}>Pagamentos</a></div>
        <div class="shadow-none p-3 m-3 bg-light rounded"><a href="#" class="nav-link" style="display: block">Publicar</a></div>
    </div>
    <div style="height: 100%; width: 80%; position: absolute; top: 0; right: 0;">
        {#if main_tab=="home"}
            <Home/>
        {:else if main_tab=="admin"}
            <Admin/>
        {/if}
    </div>
</main>
