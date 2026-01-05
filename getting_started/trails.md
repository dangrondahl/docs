---
title: "Trails"
description: "Learn about Kosli Trails, how to create and manage them."
icon: "route"
---

Every time you execute a process represented by a Kosli Flow, you would initiate a `trail` to record the changes made during that specific execution.

You have the flexibility to determine the boundaries of what you consider a single execution of your process. For instance, in a software delivery process, an execution instance might be defined by:

<AccordionGroup>
  <Accordion title="Git commits" icon="code-commit">
    The trail represents changes recorded from a single commit (as reported from CI).
  </Accordion>
  <Accordion title="Pull requests" icon="code-pull-request">
    The trail represents changes recorded throughout the life of a single pull request (can span multiple commits).
  </Accordion>
  <Accordion title="Jira or Github issues" icon="list-check">
    The trail represents changes recorded throughout the life of a single ticket/issue (can span multiple pull requests and commits).
  </Accordion>
</AccordionGroup>

Each trail must possess a unique name within the Flow. This name typically follows a custom pattern, depending on how you define the scope of a single process execution.

## Begin a trail

To begin a Trail, you can run a command similar to the one below:

```shell
kosli begin trail trail-1 --flow process-1 --description "My first trail"
```

Rerunning the command with different description or template file will update the Trail.

See [kosli begin trail](/client_reference/kosli_begin_trail/) for more details.

<Note>
You can overwrite the flow template for each trail using `--template-file`.
By default, the trail inherits the template from its Flow.
</Note>
