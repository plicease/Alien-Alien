# Alien::Alien [![Build Status](https://secure.travis-ci.org/plicease/Alien-Alien.png)](http://travis-ci.org/plicease/Alien-Alien)

Find or use alien package conversion tool

# SYNOPSIS

    use Alien::Alien;
    use Env qw( @PATH );
    
    unshift @ENV, Alien::Alien->bin_dir;
    
    system "alien --to-rpm --scripts ./mkpkg.deb";

# DESCRIPTION

This [Alien](https://metacpan.org/pod/Alien) module provides the `alien` tool that converts between different
Linux package formats.  Reading this documentation, and seeing the name, you may
feel as though you are glancing through the looking glass.  This distribution is
not _entirely_ a joke, though it is somewhat to tongue in cheek.  One of the useful
things that this module provides is some interesting challenges in the [Alien](https://metacpan.org/pod/Alien)
space.  That includes

- Tool is implemented as Perl

    `alien` is implemented in Perl, and distributed as a standard CPAN style distribution,
    but isn't available ON CPAN.

- Project is hosted on SourceForge

    This module drove development of [Alien::Build::Plugin::Decode::SourceForge](https://metacpan.org/pod/Alien::Build::Plugin::Decode::SourceForge), which I
    expect will be useful for other Aliens.

- Tool is architecture independent

    Aliens using [Alien::Build](https://metacpan.org/pod/Alien::Build) are usually installed in the architecture specific library
    location, because they _usually_ are architecture specific.  Since this tool is Perl,
    it is architecture independent, so we install it in the regular architecture independent
    library location.

- Project is distributed as a tar.xz file.

    This is an added complication and sort of a hassle for a few bytes saved.  Thanks!

# METHODS

## bin\_dir

    my @dirs = Alien::Alien->bin_dir;

Returns the list of directories that need to be added to the PATH in order for `alien`
to work.  This may be an empty list (as for a system install).

# SEE ALSO

- [Alien](https://metacpan.org/pod/Alien)
- [alienfile](https://metacpan.org/pod/alienfile)
- [Alien::Build](https://metacpan.org/pod/Alien::Build)
- [Alien::Base](https://metacpan.org/pod/Alien::Base)

# AUTHOR

Graham Ollis <plicease@cpan.org>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2017 by Graham Ollis.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
