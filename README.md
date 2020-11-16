# Usando WebSocket Backend

-[ ] Criar pasta 'Hub'
-[ ] Criar uma nova classe na pasta [SignalHub]
-[ ] A nova classe deve herdar de  `Hub`
-[ ] Startup adicionar o servico do SignalR (services.AddSignalR();)
-[ ] Mapeando o servico 

>app.UseSignalR(r => 
{
    r.MapHub<SignalHub>("/signalhub")
});
### Controller
-[ ] Criar o controller com a injecao do IHubContext
>private readonly IHubContext<SignalHub> _hub;

-[ ] Enviar

>_hub.Clients.Others.SendAsync(" ", " ");