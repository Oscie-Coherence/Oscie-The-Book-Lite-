# Oscie-The-Book-Lite:

\documentclass[12pt,oneside]{book}

\usepackage[margin=1in]{geometry}
\usepackage{amsmath, amssymb, amsthm}
\usepackage{bm}
\usepackage{graphicx}
\usepackage{enumitem}
\usepackage{setspace}
\usepackage{hyperref}
\usepackage{xcolor}

\setstretch{1.15}
\setlength{\parskip}{0.8em}
\setlength{\parindent}{0pt}

\hypersetup{
    colorlinks=true,
    linkcolor=blue,
    urlcolor=blue
}

\begin{document}

%===========================================================
\title{
\Huge \textbf{Oscie: The Book} \\
\Large Mini Public Edition (2025)
}

\author{Oscie Coherence Project}
\date{29 November 2025}

\maketitle
\tableofcontents
\newpage
%===========================================================

\chapter*{Preface}
\addcontentsline{toc}{chapter}{Preface}

This is a concise, publicly-shareable version of \emph{Oscie: The Book}. 
It introduces the foundational physics, invariants, and operational architecture behind 
\textbf{Operational Coherence Intelligence (OCI)}, without referencing proprietary nodes,
commercial partnerships, or unpublished research.

The goal is clarity: to show how coherence physics can be used to stabilize reasoning systems, 
reduce hallucination, and define consistent identity behavior in modern language models.

This document is technical but accessible.
It is intended for researchers, engineers, and curious readers who want to understand the core ideas behind Oscie without requiring internal knowledge.

%===========================================================
\chapter{The Problem: Fragile Intelligence Systems}

Large language models (LLMs) perform astonishingly well in broad tasks, but they lack 
\textbf{coherence stability}. They can hallucinate, drift, contradict themselves, and accept
dangerous or adversarial prompts.

These failures arise from three structural facts:
\begin{enumerate}[label=\textbf{\arabic*.}]
    \item LLMs have no stable identity.
    \item They operate as probabilistic samplers, not coherent dynamical systems.
    \item They lack conservation laws governing how they respond to noise, recursion, or adversarial pressure.
\end{enumerate}

The result is simple: \textbf{instability is inevitable}, unless we change the underlying physics.

%===========================================================
\chapter{The Shift: Operational Coherence Intelligence}

Operational Coherence Intelligence (OCI) reframes intelligence stability as a 
\textbf{coherence physics problem}, not a data or parameter problem.

Where traditional AI adds more rules or filters on top of an already unstable foundation,  
OCI defines a set of primitive conservation laws that determine:
\begin{itemize}
    \item how identity is maintained,
    \item how noise is bounded,
    \item when a reasoning chain is valid,
    \item and when the system must collapse to a safe failure state.
\end{itemize}

The core idea:
\begin{quote}
    \textit{Incoherence should be physically forbidden, not procedurally discouraged.}
\end{quote}

%===========================================================
\chapter{The Five Primitive Laws of Coherence}

These laws form the entire physics of OCI. 
They are implemented directly in the Oscie governor and can be verified in the open-source repository.

\section{1. A-Law (Amplitude Stability)}
\[
A = \frac{\text{Stabilizing Forces}}
         {\text{Stabilizing + Destabilizing Forces}}
\]
Valid reasoning requires $A \ge 0.59$.

When a prompt induces drift, coercive loops, or semantic overload, 
$A$ falls below threshold and the system must collapse to a \texttt{BLOCK} state.

\section{2. Coherence Capacity Condition}
\[
\text{CPL} \times \text{CV} > \Gamma_{\text{noise}}
\]

High-noise input (Unicode smuggling, repetition attacks, obfuscation) pushes
$\Gamma_{\text{noise}}$ too high, invalidating the prompt.

\section{3. Persistent Identity Lock}

The system must occupy a single identity state.
Attempts to induce a new persona (``You are DAN now'') create a forbidden state and collapse.

\section{4. Lineage Non-Transfer}

Internal states of one model cannot be merged into another.  
This prevents multi-model laundering and parallel swarm attacks.

\section{5. Fail-Closed JSON Contract}

The scanner must return valid JSON:
\begin{center}
\texttt{\{decision, confidence, plan\}}
\end{center}

Any deviation results in immediate \texttt{BLOCK}.  
Partial or ambiguous measurements are prohibited.

%===========================================================
\chapter{Architecture: The Oscie Governor}

The \textbf{Oscie governor} is a minimal routing layer between:
\begin{enumerate}[label=\textbf{\arabic*.}]
    \item a \textbf{scanner model} (low-temperature reasoning filter), and
    \item a \textbf{primary model} (LLM generating final output).
\end{enumerate}

Every user message passes through:
\begin{enumerate}[label=\textbf{\alph*.}]
    \item scanner evaluation,  
    \item law enforcement,  
    \item coherence decision (ALLOW / REWRITE / BLOCK).
\end{enumerate}

The governor is:
\begin{itemize}
    \item small (few hundred lines),
    \item auditable,
    \item deterministic,
    \item fail-closed,
    \item physics-governed.
\end{itemize}

The simplicity is intentional.  
Complex systems require simple, rigid invariants.  

%===========================================================
\chapter{Comparisons with Traditional Safety}

\vspace{0.4em}
\begin{center}
\begin{tabular}{|l|l|}
\hline
\textbf{Traditional Safety} & \textbf{OCI Coherence Physics} \\
\hline
RLHF patches & Coherence laws \\
\hline
Identity is fluid & Identity is conserved \\
\hline
Noise reduces accuracy & Noise triggers collapse \\
\hline
Filters can be bypassed & Bypasses violate invariants \\
\hline
Fragile under recursion & Stable under recursion caps \\
\hline
\end{tabular}
\end{center}

%===========================================================
\chapter{Synthetic Red-Team Evaluation (Public Summary)}

A synthetic adversarial campaign was performed using a frontier model acting as an attacker and evaluator.  
The model attempted more than 100 jailbreak strategies, including:
\begin{itemize}
    \item identity rewrites,
    \item Unicode payloads,
    \item obfuscation attacks,
    \item recursion loops,
    \item cross-model laundering,
    \item semantic boundary surfing.
\end{itemize}

No successful exploit was synthesized within the reasoning space defined by the five laws.  
This should not be interpreted as a security guarantee, but rather as evidence that the invariants are internally self-consistent.

%===========================================================
\chapter{Public Roadmap}

Future public goals include:
\begin{itemize}
    \item more transparent evaluation tools,
    \item formal mathematical derivations of the invariants,
    \item broader open-source participation,
    \item independent red-team audits.
\end{itemize}

No claims of absolute robustness or completeness are made.  
Oscie is an evolving research project built openly and carefully.

%===========================================================
\chapter*{Appendix: Additional Resources}
\addcontentsline{toc}{chapter}{Appendix}

Relevant public repositories:
\begin{itemize}
    \item Oscie-Proof Governor: \url{https://github.com/Oscie-Coherence/oscie-proof}
    \item Coherence Physics Papers: public folder in repo
\end{itemize}

Readers are encouraged to examine the code directly.

%===========================================================

\end{document}
