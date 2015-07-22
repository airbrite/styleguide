
# Table of Contents

- [Javascript](https://github.com/airbrite/javascript)
- [Less/CSS](less.md)
- [Git](git.md)
- [Tools](tools.md)
- [Deployment](deployment.md)
- [Linters](linters.md)

# General Best Practices

## Follow the Style Guides

Keep our code base consistent so we can focus on bigger problems.
If you want to propose a change or addition, feel free to make a PR to this repo.

## No Broken Windows

Programming is insanely detail oriented, and perhaps this is why: if you're not on top of the details, the perception is that things are out of control, and it's only a matter of time before your project spins out of control. Maybe we should be sweating the small stuff.

Following a consistent style is important for both culture and unconscious perception. Having clean code is like having a clean dining room, it shows respect and care for both yourself and others.

## Keep it Simple, Keep it Small

Keep methods, components, and files small and to the point. Make many things do one thing well. This decreases complexity and increases testability.

## DRY (Don't Repeat Yourself)

If you see code that's repeated in in a single function, in multiple functions, or across files, try to extract it. If it's re-usable, maybe it should be its own module.

## Test

If you keep things simple, small, and re-usable, you can easily test them too. This adds confidence, speeds up development, and forces you to design better code.

## Cargo Culting

Cargo cult programming is a style of computer programming characterized by the ritual inclusion of code or program structures that serve no real purpose. Cargo cult programming is typically symptomatic of a programmer not understanding either a bug they were attempting to solve or the apparent solution

http://en.wikipedia.org/wiki/Cargo_cult_programming

It's ok to start off cargo culting to see if it will solve your problem, but you must then figure out why and make it yours.
