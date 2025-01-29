# The Perfect Project Template
A Template for the Perfect Project

```bash
/
├── .ci/
│   └── scripts/
├── .git/
├── .gitignore
├── .tool-versions
├── .deploy/
├── └── scripts/
├── .build/
├── └── scripts/
├── GETTING_STARTED.md
├── Makefile
├── README.md
├── src/
└── ...
```

An informed view on the generalized structure for a project folder. If it can be built, run, or generates an artifact some or all of this is the right choice.

### Reasoning

At each level we are creating a little border around the tools and patterns we use, creating a project protocol if you will. So projects can be more interchangeable and better to keep them simple. We are intentionally saying "don't think about it just follow this pattern." While this might feel like overstepping into someone elses agency it should feel more like a relief because its a decision you don't have to make and ultimately you are not bound to. We should invite a repeatable protocol because being clever is like getting a puppy, its a lot of responsibility.

We started this discussion deep in the type of tooling but in reality this is about knowledge artifacts. We are trying to answer the following questions with our protocol:
- what version of x do I need to install
- how do I boot this up
- how do I deploy this
- how do I build this
- how do CI/Gitops/Automation happen

I have done all that without having to ensure someone already knows and better yet if they have seen a project they already know.

### Explanation

Put how manual steps and explanation for your projects setup by a dev in `GETTING_STARTED.md`

Put how to use and operated in `README.me`

Use tools like [ASDF](https://asdf-vm.com/) or [MISE](https://github.com/jdx/mise) to track your runtime dependencies in `.tool-versions`

Keep deploy scripts and details like k8s charts in `.deploy`

Keep build scripts and other tools in `.deploy`

Keep Ci and Automation stuff in `.ci`

Link it all with the Makefile

Expose:
- make init
- make build
- make deploy
- make test

PARTY!
