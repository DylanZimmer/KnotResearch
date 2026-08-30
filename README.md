# KnotResearch

An interactive research tool for exploring knots, manipulating knot diagrams, and studying the behavior of knot invariants under sequences of manipulations.

knotresearch.netlify.app

**Note:** The backend may take a moment to start if it has been inactive.

KnotResearch is a full-stack application for computational experimentation in knot theory in two ways. The first is to allow a user to manipulate knot diagrams and observe how the diagram changes, along with the corresponding changes in its invariants. The second is to allow for experiments: sequences of moves can be applied to sets of knots until an end step or goal is reached, while preserving the history of the intermediate steps. The intention is to use the resulting data to explore and investigate broader patterns in knot theory.

## Current Features

### Knot Exploration

KnotResearch currently provides access to knots from the **Rolfsen table up to 13 crossings**. Knots can be generated and explored individually through the application.

### Oriented Knot Diagrams

Knot diagrams are represented as structured data rather than simply as images. The application maintains information about crossings, strands, orientations, and the relationships between them, allowing diagrams to be manipulated computationally.

### Diagram Manipulation

The application supports transformations of knot diagrams, including:

* Changing the orientation of a knot
* Taking the mirror image of a knot
* Applying Reidemeister moves
* Smoothing
* Saddle operations

These operations allow users to investigate how different manipulations affect both the diagram and its associated invariants.

### Invariant Computation

Knot invariants are computed and associated with the knots and diagrams being explored. This makes it possible to compare the state of a knot before and after a sequence of transformations.

## Research Experiments

The goal of KnotResearch is to provide a framework for running experiments across collections of knots.

The application is intended to preserve the intermediate states and transformations along the way, making it possible to construct datasets describing how knots and their invariants change throughout an experiment.

## Architecture

KnotResearch consists of a React/TypeScript frontend and a Spring Boot backend, with PostgreSQL providing persistent storage.

'''
┌──────────────────────────┐
│    React / TypeScript    │
│         Frontend         │
└────────────┬─────────────┘
             │
             │ REST API
             ▼
┌──────────────────────────┐
│      Spring Boot         │
│        Backend           │
└────────────┬─────────────┘
             │
       ┌─────┴─────┐
       ▼           ▼
 PostgreSQL    Mathematical
 / Supabase    Computation
 '''

## Technology

**Frontend**

* React
* TypeScript
* Vite
* Tailwind CSS

**Backend**

* Java 17
* Spring Boot
* Maven

**Mathematical Computing**

* Python
* SageMath
* SnapPy

**Database**

* PostgreSQL
* Supabase

## Repositories

### Frontend

The React/TypeScript application responsible for the user interface, knot visualization, and interaction.

https://github.com/DylanZimmer/KnotResearchFrontend

### Backend

The Spring Boot application responsible for the REST API, database interaction, diagram data, and research operations.

https://github.com/DylanZimmer/KnotResearchBackend

## Development

KnotResearch is actively under development. Current work is focused on expanding the diagram manipulation engine, improving the reliability of transformations, and developing the infrastructure needed to run and analyze experiments across collections of knots.
