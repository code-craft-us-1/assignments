# Modularity recap

[Intuitive file names](https://github.com/code-craft-us-1/well-named-in-cpp-srirenukachaluvadi/pull/1/files)

[Separation](https://github.com/code-craft-us-1/well-named-in-cpp-jayydev/pull/1/files) of formatting from printing

[Separation](https://github.com/code-craft-us-1/well-named-in-cpp-nageshwariK/pull/1/files) of reading and writing

## A case against generic naming

Be careful of files whose name ends in `Utility`, `Manager`, `Handler`, `Helper`

It means you are not clear about the contents of the file.
Single Responsibility would be violated. The file would end up attracting unrelated functionality.
