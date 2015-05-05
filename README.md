Xcode-Configuration
===================

Xcode projects are just a pain to be configured properly and include the many different settings on different levels. This project is meant to help everyone with different configurations, schemes and options by giving some idea of how projects can be configured. It contains examples, xcconfig files for different kind of situations, guides and ideas, while trying to keep universal scheme at the top level.

# Motivation

After working with iOS projects for a while, I've been struggling to find a good option to setup my projects. There are just many too configuration options available. While you can set everything manually by configuring Xcode project, there are still some better options and even then many questions of how the settings can be grouped. In Xcode we have:

- Schemes (shared or user)
- Targets (products)
- Build configurations (Debug, Release)
- xcconfig files (what are those?)

But all we know is what we want project to have:
- Multiple environments with specific variables (URL for example).
- Debug settings that include different libraries.
- Different app names, so can allow multiple apps to be installed at same time (Ad-Hoc and App Store versions).
- Many libraries with CocoaPods.
- Very strict environment (all warnings are errors, most warnings enabled in compiler).
- Easy addition and editing of new environments.
- Specific configuration for code quality checks (such as Faux Pas).

We also know what we do not want to have:
- Same settings in multiple places.

*The question remains. How do we use every available option to create a stable and easy to use project structure?*


# The Solution

I began looking for a solution in multiple open source projects, including:
- https://github.com/jspahrsummers/xcconfigs
- https://github.com/krzysztofzablocki/KZBootstrap

All projects from here are solving at least one situation which I needed, but none of them were a complete solution, at least not for my case.

The configuration part of the solution is based mostly on structured .xcconfig files, from multiple reasons:
- Inheritance!
- Easily extendable.
- Easily editable.