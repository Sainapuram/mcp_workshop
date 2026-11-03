# MCP Workshop — Assignment Answers

### 1. How many tools did the server list in Part 1 and Part 3? What did you have to change in the client?

In Part 1, the server listed 8 tools. After I added the `predict_both` tool, it listed 9 tools in Part 3.

I did not need to change the client to register the new tool. The client automatically discovered it when it requested the available tools from the server.

### 2. On how many of the 114 test patients do the models disagree? Which model was correct?

The two models disagreed on 8 out of 114 test patients.

| Patient | Correct Model |
|---|---|
| 3 | Logistic Regression |
| 25 | Logistic Regression |
| 48 | Logistic Regression |
| 53 | KNN |
| 76 | Logistic Regression |
| 80 | Logistic Regression |
| 99 | Logistic Regression |
| 102 | Logistic Regression |

### 3. Overall, which model was right more often when they disagreed?

Logistic Regression was correct for 7 of the 8 disagreements, while KNN was correct for only 1. Therefore, Logistic Regression performed better on the patients where the models disagreed.

### 4. Why does the description in triple quotes matter when an AI app uses this tool?

The description explains what the tool does. When an AI application discovers the available MCP tools, it can read their descriptions to understand their purposes and decide which tool to use for a particular task.

For example, the `predict_both` description tells the AI that the tool runs both models and checks whether their predictions agree.

### 5. Why is it useful for the server to log every tool call?

Logging every tool call helps us track which tool was used, when it was called, and whether it succeeded or failed. This makes it easier to identify errors, debug problems, and verify that the tools are working correctly.

In this assignment, the audit log helped me confirm that the `predict_both` calls were executed successfully.