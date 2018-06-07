# wast-sublime-syntax

WAST, the [text format][1] of [WebAssembly][2], is a very low-level but
human-readable and writable stack-based language. It is a tree of
[s-expressions][3], generally, though instructions can also be written linearly.

This is a [Sublime Syntax][4] definition for WAST. It requires
[Sublime Text version 3][5] or greater.

<!-- MarkdownTOC autolink=true -->

- [Highlighting examples](#highlighting-examples)
- [Symbols](#symbols)
- [Other meta-features](#other-meta-features)
- [Scopes](#scopes)
- [Limitations](#limitations)

<!-- /MarkdownTOC -->

## Highlighting examples

Using the themes Monokai, Propeller, Welded, and Excelsior
(from [ES Sublime][6]) respectively:

![Using Monokai](https://github.com/bathos/wast-sublime-syntax/raw/master/examples/monokai.png)
![Using Propeller](https://github.com/bathos/wast-sublime-syntax/raw/master/examples/propeller.png)
![Using Welded](https://github.com/bathos/wast-sublime-syntax/raw/master/examples/welded.png)
![Using Excelsior](https://github.com/bathos/wast-sublime-syntax/raw/master/examples/excelsior.png)

I haven’t included any customized themes presently. I may add one later that
highlights s-expressions by depth, since I think it would be an interesting
experiment.

## Symbols

Functions, globals and types will appear in the local symbol list if they have
been given names, but not if they’re anonymous (that is, only referenced by
index).

Exports will appear in both the local and global symbol lists.

## Other meta-features

There is a definition for comments but, presently, no definition for indents. I
still don’t know quite what that should look like — there seem to be some very
different approaches to formatting s-expressions in the wild and I don’t have
enough context yet to know which to choose. (Feedback or PRs welcome.)

## Scopes

The following scopes are provided. Mostly this sticks to TextMate conventions
but with additional precision in some cases and, for certain stuff, minor abuse
of not-quite-applicable-but-common scopes in order to help improve compatibility
with existing color schemes. In particular, I used `storage.type.constant` in
order to force distinct coloring for some things that are semantically not all
“constant”.

- `comment.block.wast`
- `comment.line.wast`
- `constant.character.escape.byte.wast`
- `constant.character.escape.char.wast`
- `constant.numeric.float.wast`
- `constant.numeric.integer.wast`
- `entity.name.export.wast`
- `entity.name.function.wast`
- `entity.name.memory.wast`
- `entity.name.module.import.wast`
- `entity.name.module.wast`
- `entity.name.statement.wast`
- `entity.name.table.wast`
- `entity.name.type.wast`
- `invalid.illegal.wast`
- `keyword.control.conditional.wast`
- `keyword.control.flow.wast`
- `keyword.declaration.offset.wast`
- `keyword.operator.assignment.wast`
- `keyword.operator.word.wast`
- `keyword.other.export.wast`
- `keyword.other.import.wast`
- `keyword.other.module.wast`
- `keyword.other.offset.wast`
- `keyword.other.start.wast`
- `meta.block.conditional.wast`
- `meta.block.loop.wast`
- `meta.block.wast`
- `meta.function-call.wast`
- `meta.group.limit.wast`
- `meta.invocation.wast`
- `meta.s-expression.data.wast`
- `meta.s-expression.elem.wast`
- `meta.s-expression.export-description.wast`
- `meta.s-expression.export.wast`
- `meta.s-expression.expression.wast`
- `meta.s-expression.function.wast`
- `meta.s-expression.functype.wast`
- `meta.s-expression.global.wast`
- `meta.s-expression.globaltype.wast`
- `meta.s-expression.import.wast`
- `meta.s-expression.instruction.wast`
- `meta.s-expression.local.wast`
- `meta.s-expression.memory.wast`
- `meta.s-expression.module.wast`
- `meta.s-expression.offset.wast`
- `meta.s-expression.param.wast`
- `meta.s-expression.result.wast`
- `meta.s-expression.start.begin.wast`
- `meta.s-expression.table.wast`
- `meta.s-expression.type.wast`
- `meta.s-expression.typeuse.wast`
- `punctuation.definition.block.begin.wast`
- `punctuation.definition.block.conditional.begin.wast`
- `punctuation.definition.block.conditional.end.wast`
- `punctuation.definition.block.end.wast`
- `punctuation.definition.block.loop.begin.wast`
- `punctuation.definition.block.loop.end.wast`
- `punctuation.definition.comment.begin.wast`
- `punctuation.definition.comment.end.wast`
- `punctuation.definition.data.begin.wast`
- `punctuation.definition.data.end.wast`
- `punctuation.definition.elem.begin.wast`
- `punctuation.definition.elem.end.wast`
- `punctuation.definition.export.begin.wast`
- `punctuation.definition.export.end.wast`
- `punctuation.definition.exportdesc.begin.wast`
- `punctuation.definition.exportdesc.end.wast`
- `punctuation.definition.expression.begin.wast`
- `punctuation.definition.expression.end.wast`
- `punctuation.definition.function.begin.wast`
- `punctuation.definition.function.end.wast`
- `punctuation.definition.functype.begin.wast`
- `punctuation.definition.functype.end.wast`
- `punctuation.definition.global.begin.wast`
- `punctuation.definition.global.end.wast`
- `punctuation.definition.globaltype.begin.wast`
- `punctuation.definition.globaltype.end.wast`
- `punctuation.definition.import.begin.wast`
- `punctuation.definition.import.end.wast`
- `punctuation.definition.instruction.begin.wast`
- `punctuation.definition.instruction.end.wast`
- `punctuation.definition.local.begin.wast`
- `punctuation.definition.local.end.wast`
- `punctuation.definition.memory.begin.wast`
- `punctuation.definition.memory.end.wast`
- `punctuation.definition.module.begin.wast`
- `punctuation.definition.module.end.wast`
- `punctuation.definition.offset.begin.wast`
- `punctuation.definition.offset.end.wast`
- `punctuation.definition.param.begin.wast`
- `punctuation.definition.param.end.wast`
- `punctuation.definition.result.begin.wast`
- `punctuation.definition.result.end.wast`
- `punctuation.definition.start.begin.wast`
- `punctuation.definition.start.end.wast`
- `punctuation.definition.string.begin.wast`
- `punctuation.definition.string.end.wast`
- `punctuation.definition.table.begin.wast`
- `punctuation.definition.table.end.wast`
- `punctuation.definition.type.begin.wast`
- `punctuation.definition.type.end.wast`
- `punctuation.definition.typeuse.begin.wast`
- `punctuation.definition.typeuse.end.wast`
- `source.wast`
- `storage.modifier.mutable.wast`
- `storage.modifier.result.wast`
- `storage.modifier.type.wast`
- `storage.modifier.wast`
- `storage.type.constant.wast`
- `storage.type.data.wast`
- `storage.type.elem.wast`
- `storage.type.function.wast`
- `storage.type.global.wast`
- `storage.type.local.wast`
- `storage.type.memory.wast`
- `storage.type.param.wast`
- `storage.type.table.wast`
- `storage.type.type.wast`
- `string.quoted.double.wast`
- `support.function.memory.wast`
- `support.function.numeric.wast`
- `support.function.variable.wast`
- `support.type.wast`
- `variable.other.index.wast`
- `variable.other.readwrite.wast`
- `variable.other.wast`
- `variable.parameter.wast`

## Limitations

As with most languages, Sublime Syntax and Text Mate syntax definitions can
model WAST correctly at the lexical level, but newline blindness prevents ideal
scoping of some constructs.

In this case, however, there are not many issues that arise from this — really
there’s just one. Whenever "(" is followed by a keyword, if there is a newline
or a multiline comment between them, this syntax definition will not match that
s-expression correctly. Since it would be unusual/unreadable if there really
were newlines or comments in that position, I haven’t included any special
recovery logic, only this caveat emptor.

Some higher level syntactic constraints are applied, like only allowing one
_start_ field, but plenty of other well-formedness constraints are not applied,
even where they technically could be expressed in terms of Sublime Syntax.

[1]: https://webassembly.github.io/spec/core/text/index.html
[2]: https://webassembly.github.io/spec/core/index.html
[3]: https://en.wikipedia.org/wiki/S-expression
[4]: https://www.sublimetext.com/docs/3/syntax.html
[5]: https://www.sublimetext.com/3
[6]: https://github.com/bathos/Ecmascript-Sublime
