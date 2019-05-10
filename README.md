# Summary

The Italian corpus annotated according to the UD annotation scheme was obtained by conversion from ISDT (Italian Stanford Dependency Treebank), released for the dependency parsing shared task of Evalita-2014 (Bosco et al. 2014).

# Introduction

ISDT is a resource annotated according to the Stanford dependencies scheme (de Marneffe et al. 2008, 2013a, 2013b, 2014), obtained through a semi-automatic conversion process starting from MIDT (the Merged Italian Dependency Treebank). MIDT, in turn, is the result of a previous effort in the direction of improving interoperability of data sets available for Italian by harmonizing and merging two existing dependency–based resources, differing both in corpus composition and adopted annotation schemes, namely:

* TUT, the Turin University Treebank (Bosco et al. 2000);
* ISST-TANL, first released as ISST-CoNLL for the CoNLL-2007 shared task (Montemagni, Simi 2007), which was developed as a joint effort by the Istituto di Linguistica Computazionale (ILC–CNR) and the University of Pisa and originating from the Italian Syntactic–Semantic Treebank (ISST, Montemagni et al. 2003).

The details of the harmonization and conversion process leading to MIDT are discussed in (Bosco, Montemagni, Simi, 2012). The Stanford annotation scheme, obtained from an enriched version of MIDT, was adapted to the specificity of the Italian language. We refer to (Bosco, Montemagni, Simi, 2013 and 2014) for a discussion.

# Acknowledgments

We wish to thank all of the contributors to the original annotation efforts, as well as the supporting organizations, i.e. the Institute for Computational Linguistics "A. Zampolli", the University of Pisa, and the University of Torino. Thanks go to Chiara Alzetta and Giulia Venturi for the good work in defining the error detection methodology and the manual revision / correction of automatically identified errors in Version 2.1.


# Main contributors

* Cristina Bosco - Università di Torino, Dipartimento di Informatica
* Alessandro Lenci - Università di Pisa, Dipartimento di Filologia, Letteratura, Linguistica
* Simonetta Montemagni - Istituto di Linguistica Computazionale A. Zampolli, CNR, Pisa
* Maria Simi - Università di Pisa, Dipartimento di Informatica

# Corpus composition

<table>
<tr style="background-color: #eee"><th>Original format</th><th>Source</th><th>Genre</th><th>Size in tokens</th><th>Size in sentences</th>
</tr>
<tr><td>TUT-CONLL</td><td>Evalita 2011 Dependency parsing</td><td>Legal texts, news articles, Wikipedia articles</td><td>101,309</td><td>3,842</td></tr>
<tr><td>ISST-TANL</td><td>Evalita 2011 Domain adaptation task</td><td>Newspaper articles</td><td>80,967</td><td>4,135</td></tr>
<tr><td>ISST-TANL</td><td>SPLeT 2012 </td><td>Legal texts: European directives</td><td>6,166</td><td>260</td></tr>
<tr><td>MIDT</td><td>Several QA competitions</td><td>Questions</td><td>20,680</td><td>2,228</td></tr>
<tr><td>MIDT</td><td>Evalita 2014 Dependency parsing:test data set (partial)</td><td>News articles</td><td>7,618</td><td>304</td></tr>
<tr><td>TUT-CONLL</td><td>Parallel TUT (Italian part)</td><td>Various genres</td><td>55,942</td><td>2,131</td></tr
<tr><td>UD</td><td>Due Parole</td><td>Simplified Italian news</td><td>24,977</td><td>1,421</td></tr>
<tr><td>UD2</td><td>New data</td><td>Various sentences</td><td>2,504</td><td>150</td></tr>
</table>

Sentences ids explicitly mark the source of the sentence.

# Corpus splitting

The Corpus (14,167 sentences; 278,429 tokens; 298,344 words) has been randomly split as follows:

* it-ud-train.conllu: 257616 tokens (13121 sentences)
* it-ud-dev.conllu: 11133 tokens (564 sentences)
* it-ud-test.conllu: 9680 tokens (482 sentences)

# Changelog

* 2019-05-1 v2.4
  * validated with stricter validation script

* 2018-11-01 v2.3
  * added enhanced dependencies

* 2018-04-01 v2.2
  * Repository renamed from UD_Italian to UD_Italian-ISDT.
  * Additional corrections of 1340 arcs, specifically:
    - 525 arcs retrieved with the methodology already used in the previous release, applied to the rest of the treebank;
    - 815 non-projective arcs were also corrected.
  * Added to the train set a new section of 2Parole, a newspaper of simplified Italian texts (283 sentences, 4985 tokens)

* 2017-11-01 v2.1
  * Corrected 786 dependency errors distributed into 567 sentences:
    * Auxiliary verbs erroneously treated as head of a dependency relation
    * Bare past participles functioning as adjectival modifiers of nouns erroneously annotated as clausal modifiers
    * Adjectives functioning as secondary predicates erroneously annotated as adjectival modifiers
    * Coordinating conjunctions erroneously headed by the first conjunct
    * Oblique nominal arguments erroneously annotated as nominal modifiers
    * Nonfinite verbs functioning as nominals erroneously annotated as oblique nominals
  * Consistency in the treatment of fixed multi-word expressions has been checked and improved.

* 2017-02-15 v2.0
  * Changes to comply with V2.
  * Splitting revised to comply with shared task.

* 2016-11-01 v1.4
  * Complete revision of the treatment of clitic pronouns
  * Added dependency subtype expl:pass, used in passive constructions
  * Added a new collection of texts from 2Parole, a newspaper of simplified Italian texts (25995 tokens)

* 2016-05-01 v1.3
  * Added feature value PronType=Ord for ordinal pronouns
  * Added feature value PronType=Predet for predeterminers
  * Added feature value NumType=Range
  * Added feature value NumType=Gen
  * Added sentence full text as comment
  * Added SpaceAfter=No, needed for recovering original text
  * Fixed errors found running content validation queries

* 2015-11-01 v1.2
  * Added dependencies expl:impers as specialization of expl for impersonal clitic pronouns
  * Fixed case in articulated preposition, previously lost during splitting
  * More fixes to xcomp/ccomp distinction
  * Harmonization of case marking for infinitive verbs introduced by articles
  * Harmonization of Light Verb constructions
  * Eliminated duplicated sentences and overlappings train/dev and train/test
  * Added short sentences to train

* 2015-05-15 v1.1
  * Added Italian section of ParTUT (71645 tokens)
  * Checked SYM
  * Checked X
  * Added more negation adverbs
  * Eliminated Gender=Com and Number=Com
  * Eliminated Negation=Neg
  * Added language specific feature PronType=Clit
  * Changed 'case' into 'mark' for 'xcomp'
  * Fixed xcomp/ccomp distinction
  * Checked dependencies marked 'dep', and resolved most of them

# References

* Cristina Bosco, Vincenzo Lombardo, Leonardo Lesmo, Daniela Vassallo. 2000.
  [Building a treebank for italian: a data-driven annotation schema](http://www.di.unito.it/~bosco/publicat/lrec00.zip). In *Proceedings of LREC 2000*, Athens, Greece.

* Cristina Bosco, Simonetta Montemagni, Maria Simi. 2012. [Harmonization and Merging of two Italian Dependency Treebanks, Workshop on Merging of Language Resources](http://www.lrec-conf.org/proceedings/lrec2012/workshops/06.LREC%202012%20Merging%20Proceedings.pdf), in *Proceedings of LREC 2012*, Workshop on Language Resource Merging, Instanbul, May 2012, ELRA, pp. 23-30.

* Cristina Bosco, Simonetta Montemagni, Maria Simi. 2013. [Converting Italian Treebanks: Towards an Italian Stanford Dependency Treebank](http://acl.eldoc.ub.rug.nl/mirror/W/W13/W13-2308.pdf). In *Proceedings of the 7th Linguistic Annotation Workshop & Interoperability with Discourse* (LAW VII & ID at ACL-2013), Sofia, Bulgaria, August 8-9, pp. 61-69.

* Cristina Bosco, Felice Dell’Orletta, Simonetta Montemagni, Manuela Sanguinetti, Maria Simi. 2014.
  [The Evalita 2014 Dependency Parsing task](http://clic.humnet.unipi.it/proceedings/Proceedings-EVALITA-2014.pdf), *CLiC-it 2014 and EVALITA 2014 Proceedings*,
  Pisa University Press, ISBN/EAN: 978-886741-472-7, pp. 1-8.

* Marie-Catherine de Marneffe and Christopher D. Manning. 2008.
  [The Stanford typed dependencies representation](http://nlp.stanford.edu/pubs/dependencies-coling08.pdf).
  In *COLING Workshop on Cross-framework and Cross-domain Parser Evaluation*.

* Marie-Catherine de Marneffe, Miriam Connor, Natalia Silveira, Bowman S. R., Timothy Dozat, Christopher D. Manning. 2013. [More constructions, more genres: Extending Stanford Dependencies](https://www.aclweb.org/anthology/W/W13/W13-37.pdf), *Proc. of the Second International Conference on Dependency Linguistics* (DepLing 2013), Prague, August 27–30, Charles University in Prague, Matfyzpress, Prague, pp. 187–196.

* Marie-Catherine de Marneffe and Christopher D. Manning. 2013. [Stanford typed dependencies manual](http://nlp.stanford.edu/software/dependencies_manual.pdf),
  September 2008, Revised for the Stanford Parser v. 3.3 in December 2013.

* Marie-Catherine de Marneffe, Timothy Dozat, Natalia Silveira, Katri
  Haverinen, Filip Ginter, Joakim Nivre, Christopher Manning. 2014.
  [Universal Stanford Dependencies: A cross-linguistic typology](http://nlp.stanford.edu/pubs/USD_LREC14_paper_camera_ready.pdf).
  In *Proceedings of LREC 2014*.

* Simonetta Montemagni, Francesco Barsotti, Marco Battista, Nicoletta Calzolari, Ornella Corazzari, Alessandro Lenci, Antonio Zampolli, Francesca Fanciulli, Maria Massetani, Remo Raffaelli, Roberto Basili, Maria Teresa Pazienza, Dario Saracino, Fabio Zanzotto, Nadia Mana, Fabio Pianesi,
and Rodolfo Delmonte. 2003. Building the Italian Syntactic-Semantic Treebank. In A. Abeillé (Ed.), Building and Using syntactically annotated corpora.
Kluwer, Dordrecht.

* Simonetta Montemagni, Maria Simi. 2007. [The Italian dependency annotated corpus developed for the CoNLL–2007 shared task](http://medialab.di.unipi.it/isst/). Technical report, ILC–CNR.

* Maria Simi, Cristina Bosco, Simonetta Montemagni. 2014. [Less is More? Towards a Reduced Inventory of Categories for Training a Parser for the Italian Stanford Dependencies](http://www.lrec-conf.org/proceedings/lrec2014/summaries/818.html). 2014. In *Proceedings of LREC 2014*, ELRA, pp. 83–90.

=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v1.0
License: CC BY-NC-SA 3.0
Includes text: yes
Genre: legal news wiki
Lemmas: converted from manual
UPOS: converted from manual
XPOS: manual native
Features: converted from manual
Relations: converted from manual
Contributors: Bosco, Cristina; Lenci, Alessandro; Montemagni, Simonetta; Simi, Maria
Contributing: elsewhere
Contact: simi@di.unipi.it
