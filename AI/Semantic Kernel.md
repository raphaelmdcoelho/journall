É uma SDK.

É um concorrente  do Autogen e o LangChain.

Package: `Microsoft.SemanticKernel`

Package: Microsoft.SemanticKernel.Connectors.Ollama

** Microsoft.Extensions.Logging / ....Logging.Console

Geralmente no ambiente dotnet, sempre temos um builder no começo.

```csharp
var builder = Kernel.CreateBuilder()
	.AddOllamChatCompletion(
		modelId: "llama3.1:latest", // tooling support
		endpoint: new Uri("http://localhost:11434"),
	);

builder.AddServces().AddLogging(x => x.AddConsole().SetMinimumLevel(LogLevel.Trace));

var app = builder.Build();

var chatCompletionService = app.GetRequiredService<IChatCompletionService>();
app.Plugins.AddFromType<CustomClass>();

OllamaPromptExecutionSettings settings = new()
{
	FunctionChoiceBehavior = FunctionChoiceBehavior.Auto()
};
...

var history = new ChatHistory();

history.AddUserMessage(input);

var result = await chatCompletionService.GetChatMessageContentAsync(
	history, 
	settings, 
	app);

history.AddMessage(result.Role, result.Content ?? String.Empty);


...

[KernelFunction("functionName")]
// It's possisble to add a description as a parameter, to facilitates the decision to use the function or not.

```

## Plugins



#tech #ai

