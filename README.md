# green_trust: A green thread rust library 


## Compiler features:
### Naked functions
https://github.com/rust-lang/rfcs/blob/master/text/1201-naked-fns.md
when Rust compiles a function, it adds a small prologue and epilogue to each function and this causes some issues for us
when we switch contexts since we end up with a misaligned stack. Once
we need to switch back to the same stack again we end up in trouble.
Marking a function as #[naked] removes the prologue and epilogue. 
