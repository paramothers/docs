------------------------------------------------------------------------

Overview
========

[General](#table0)
 [API-SpringBatch 3.0](#table1)
 [API- Job Repository](#table2)
 [API-Repeat](#table3)
 [API-Retry](#table4)
 [API-Step](#table5)
 [API- Job](#table6)
 [API-JunitTesst](#table7)
 [API-Listener](#table8)
 [API-policy & status](#table9)
 [API-ItemProcessor](#table10)
 [API-ItemReader](#table11)
 [API-ItemWriter](#table12)
 [Spring batch LLR](#table13)
 [SpringBatch-SESSION](#table14)

------------------------------------------------------------------------

Sheet 1: *General*
==================

|                                                                                                     |             |
|-----------------------------------------------------------------------------------------------------|-------------|
| **Understanding**                                                                                   |             |
|                                                                                                     |             |
| it requires                                                                                         | release     |
| Spring core – DI                                                                                    |             |
| Spring JDBC                                                                                         | 1.0 at 2008 |
| Spring Transaction management                                                                       | 2.0 at 2009 |
|                                                                                                     | 3.0 at 2014 |
|                                                                                                     |             |
| Spring batch was born in 2007                                                                       |             |
| Batch technology from ACCENTURE & Spring from SpringSource                                          |             |
|                                                                                                     |             |
|                                                                                                     |             |
|                                                                                                     |             |
|                                                                                                     |             |
| Batch job can be start from command line / HTTP request / Scheduler                                 |             |
|                                                                                                     |             |
|                                                                                                     |             |
|                                                                                                     |             |
| Job Launcher – it create state for a job before to launch                                           |             |
| Job Repository – it has state of batch jobs – repository can be reside either in Memory or Database |             |

------------------------------------------------------------------------

Sheet 2: *API-SpringBatch 3.0*
==============================

|                                                           |                        |
|-----------------------------------------------------------|------------------------|
| *study API of all step, stepexecction, execution context* |                        |
|                                                           | **StepBuilderFactory** |
|                                                           | **JobBuilderFactory**  |

------------------------------------------------------------------------

Sheet 3: *API- Job Repository*
==============================

|     |                                                |               |                        |                              |                                |     |
|-----|------------------------------------------------|---------------|------------------------|------------------------------|--------------------------------|-----|
|     |                                                |               |                        |                              |                                |     |
|     |                                                |               |                        |                              |                                |     |
|     |                                                |               |                        |                              |                                |     |
|     |                                                |               |                        |                              |                                |     |
|     |                                                | JobRepository | SimpleJobRepository    |                              |                                |     |
|     | database repository                            |               |                        | JobRepositoryFactoryBean     |                                |     |
|     | In-memory repositary                           |               |                        | MapJobRepositoryFactoryBean  |                                |     |
|     |                                                |               |                        |                              | ResourcelessTransactionManager |     |
|     |                                                |               |                        |                              |                                |     |
|     | more function with JobReposisoty               | JobOperator   | SimpleJobOperator      |                              |                                |     |
|     | used to READ only access data in JobRepository | JobExplorer   | JobExplorerFactoryBean |                              |                                |     |
|     |                                                |               |                        |                              |                                |     |
|     |                                                |               |                        |                              |                                |     |
|     | dynamically modify job's properties/manipulate | JobLocator    | JobRegistory           | MapJobRegistry               |                                |     |
|     |                                                |               |                        | JobRegistryBeanPostProcessor |                                |     |

------------------------------------------------------------------------

Sheet 4: *API-Repeat*
=====================

|                  |                             |                  |                             |
|------------------|-----------------------------|------------------|-----------------------------|
| RepeatOperations | RepeatTemplate              |                  |                             |
|                  | RepeatCallback              |                  |                             |
|                  |                             | ExceptionHandler | SimpleLimitExceptionHandler |
|                  |                             | RepeatContext    |                             |
|                  | RepeatStatus                |                  |                             |
|                  | RepeatListener              |                  |                             |
|                  | TaskExecuterRepeateTemplete |                  |                             |

------------------------------------------------------------------------

Sheet 5: *API-Retry*
====================

|                 |                  |                                |
|-----------------|------------------|--------------------------------|
| RetryOperations | RetryTemplate    |                                |
|                 | RetryCallback    |                                |
|                 |                  | RetryContext                   |
|                 | RecoveryCallback |                                |
|                 | RetryListener    |                                |
|                 | BackoffPolicy    | ExponentialBackoffPolicy       |
|                 | RetryPolicy      | SimpleRetryPolicy              |
|                 |                  | TimeoutRetryPolicy             |
|                 |                  | ExceptionClassifierRetryPolicy |

------------------------------------------------------------------------

Sheet 6: *API-Step*
===================

|                                                                                                  |                             |                     |                       |                              |                      |                             |                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------|---------------------|-----------------------|------------------------------|----------------------|-----------------------------|-----------------------------------------|
|                                                                                                  |                             |                     |                       |                              |                      |                             |                                         |
| built in command line batch launcher ( i planned to use llrbatch)                                | CommandLineJobRunner        |                     |                       |                              |                      |                             |                                         |
| it wont run, but load all jobs, wait for user to start a job, it useful when want to run by http | JobRegistryBackgroundRunner |                     |                       |                              |                      |                             |                                         |
|                                                                                                  |                             |                     |                       |                              |                      |                             |                                         |
|                                                                                                  | Step                        | FlowStep            |                       |                              |                      |                             |                                         |
|                                                                                                  |                             | JobStep             |                       |                              |                      |                             |                                         |
|                                                                                                  |                             |                     |                       |                              |                      |                             |                                         |
|                                                                                                  |                             | PartitionStep       |                       |                              |                      |                             |                                         |
|                                                                                                  |                             |                     | PartitionHandler      | TaskExecutorPartitionHandler |                      |                             |                                         |
|                                                                                                  |                             |                     | StepExecutionSplitter |                              |                      |                             |                                         |
|                                                                                                  |                             |                     | Partitioner           | SimplePartitioner            |                      |                             |                                         |
|                                                                                                  |                             |                     |                       |                              |                      |                             |                                         |
| it delete the task to any of TaskLet implementation                                              |                             | TaskletStep         | TaskLet               |                              |                      |                             |                                         |
| it is Chunk task impelementations                                                                |                             |                     |                       | ChunkOrientedTasklet         | ChunkContext         | StepContext                 |                                         |
|                                                                                                  |                             |                     |                       | CallableTaskletAdaptor       |                      |                             |                                         |
| use of exiting servie                                                                            |                             |                     |                       | MethodInvokingTaskletAdapter |                      |                             |                                         |
|                                                                                                  |                             |                     |                       | StopableTasklet              |                      |                             |                                         |
|                                                                                                  |                             |                     |                       |                              | BatchletAdaptor      |                             |                                         |
|                                                                                                  |                             |                     |                       |                              | SystemCommandTasklet | SystemProcessExitCodeMapper | ConfigurableSystemProcessExitCodeMapper |
|                                                                                                  |                             |                     |                       |                              |                      |                             | SimpleSystemProcessExitCodeMapper       |
| it represent a step execution                                                                    |                             | stepExecution       | Executioncontext      |                              |                      |                             |                                         |
|                                                                                                  |                             | StepContribution    |                       |                              |                      |                             |                                         |
| introduce new scope to postpone bean creation till step exection                                 |                             | StepScope           |                       |                              |                      |                             |                                         |
|                                                                                                  |                             |                     |                       |                              |                      |                             |                                         |
|                                                                                                  |                             |                     |                       |                              |                      |                             |                                         |
|                                                                                                  | JobExecutionDecider         | FlowExecutionStatus |                       |                              |                      |                             |                                         |
|                                                                                                  | Flow                        |                     |                       |                              |                      |                             |                                         |

------------------------------------------------------------------------

Sheet 7: *API- Job*
===================

|                                                                                                  |                             |                          |                               |                  |                             |     |             |              |                  |
|--------------------------------------------------------------------------------------------------|-----------------------------|--------------------------|-------------------------------|------------------|-----------------------------|-----|-------------|--------------|------------------|
|                                                                                                  |                             |                          |                               |                  |                             |     |             |              |                  |
| built in command line batch launcher ( i planned to use llrbatch)                                | CommandLineJobRunner        |                          |                               |                  |                             |     |             |              |                  |
| it wont run, but load all jobs, wait for user to start a job, it useful when want to run by http | JobRegistryBackgroundRunner |                          |                               |                  |                             |     |             |              |                  |
|                                                                                                  |                             |                          |                               |                  |                             |     |             |              |                  |
|                                                                                                  |                             |                          |                               |                  |                             |     |             |              |                  |
| Class implement this interface to validate the job parameters                                    |                             | JobParametersValidator   | DefaultJobParametersValidator |                  |                             |     |             |              |                  |
| to create new set of parameter from previous one                                                 |                             | JobParametersIncrementer | RunidIncrementer              |                  |                             |     |             |              |                  |
|                                                                                                  |                             |                          | JobParamertersBulider         | JobParameters    |                             |     |             |              |                  |
|                                                                                                  |                             | JobParameterExtractor    | DefaultJobParametersExtractor |                  |                             |     |             |              |                  |
|                                                                                                  |                             |                          |                               |                  |                             |     |             |              |                  |
| simple job launcher, it is begning point of a job runn                                           |                             | JobLauncher              | SimpleJobLauncher             |                  |                             |     |             |              |                  |
| it is from core-spring                                                                           |                             |                          |                               | **TaskExecutor** | \[Simple\] SyncTaskExecutor |     |             |              |                  |
|                                                                                                  |                             |                          |                               | **               
                                                                                                                                                                                             **                | SimpleAsyncTaskExecutor     | Job | SimpleJob   |              |                  |
|                                                                                                  |                             |                          |                               | **               
                                                                                                                                                                                             **                |                             |     | JobInstance | JobExecution | Executioncontext |
|                                                                                                  |                             |                          |                               |                  |                             |     |             |              |                  |
|                                                                                                  |                             |                          |                               |                  |                             |     |             |              |                  |
|                                                                                                  | Partiioner                  | ParitionHandler          | TaskExecuterPartiionHandler   |                  |                             |     |             |              |                  |
|                                                                                                  |                             |                          |                               |                  |                             |     |             |              |                  |
| dedicated job flow decider                                                                       |                             |                          |                               |                  |                             |     |             |              |                  |
|                                                                                                  |                             |                          |                               |                  |                             |     |             |              |                  |
|                                                                                                  | ExitCode                    | ExitCodeMapper           | SimpleJvmExitCodeMapper       |                  |                             |     |             |              |                  |
| exit status of job or step                                                                       |                             | ExitStatus               |                               |                  |                             |     |             |              |                  |

------------------------------------------------------------------------

Sheet 8: *API-JunitTesst*
=========================

|                                |
|--------------------------------|
| AbstractJobTest                |
| JobLauncherTestUtils           |
| StepScopeTestExecutionListener |
| stepScopeTestUtils             |
|                                |
| AssertFile                     |
|                                |
| MetadataInstanceFactory        |

------------------------------------------------------------------------

Sheet 9: *API-Listener*
=======================

|                                                               |                                   |                       |                     |
|---------------------------------------------------------------|-----------------------------------|-----------------------|---------------------|
| before and after job exection                                 | JobExecutionListener              |                       |                     |
|                                                               |                                   |                       |                     |
|                                                               | StepListener                      |                       |                     |
| we can use to load reference data and clean up reference data |                                   | StepExecutionListener |                     |
|                                                               |                                   | ChunkListener         |                     |
|                                                               |                                   |                       |                     |
| scrubbing of input data for default values or trimming        |                                   | ItemReadListener      |                     |
|                                                               |                                   | ItemProcessListener   |                     |
| some common column updates                                    |                                   | ItemWriteListener     |                     |
|                                                               |                                   |                       |                     |
|                                                               |                                   | SkipListener          | ItemSkipListener    |
|                                                               |                                   |                       | SkipListenerSupport |
|                                                               |                                   |                       |                     |
| called when a item repeated more than once                    | RepeatListener                    |                       |                     |
|                                                               | RetryListener                     | RetryListenerSupport  |                     |
|                                                               | ExecutionContextPromotionListener |                       |                     |

------------------------------------------------------------------------

Sheet 10: *API-policy & status*
===============================

|                                                                          |                    |                               |
|--------------------------------------------------------------------------|--------------------|-------------------------------|
| define own skip policy                                                   | SkipPolicy         | LimitCheckingItemSkipPolicy   |
| it is default one                                                        |                    | ExceptionClassifierSkipPolicy |
|                                                                          |                    | AlwaysSkipItemSkipPolicy      |
|                                                                          |                    | NeverSkipItemSkipPolicy       |
|                                                                          |                    |                               |
| it allow to set different commit interval on every chunk programatically | CompletionPolicy   | TimeoutTerminationPolicy      |
| it used to complete by fixed no. Of times                                |                    | SimpleCompletionPolicy        |
|                                                                          |                    | CompositeCompletionPolicy     |
|                                                                          |                    |                               |
| value rep. Step execution or job execution                               | BatchStatus        |                               |
| job launcher return this exist status object.                            |                    |                               |
|                                                                          | FlowExectionStatus |                               |
|                                                                          | ChunkListener      |                               |
|                                                                          |                    |                               |
|                                                                          |                    |                               |
|                                                                          |                    |                               |
|                                                                          |                    |                               |
|                                                                          |                    | \`                            |

------------------------------------------------------------------------

Sheet 11: *API-ItemProcessor*
=============================

|                                                         |               |                         |           |                 |
|---------------------------------------------------------|---------------|-------------------------|-----------|-----------------|
| it is optional, it transform the data, validate, filter | ItemProcessor |                         |           |                 |
| to use any existing service for processing              |               | ItemProcessorAdapter    |           |                 |
| chain of itermprocessor within single step              |               | CompositeItemProcessor  |           |                 |
|                                                         |               |                         |           |                 |
|                                                         |               | ValidatingItemProcessor |           |                 |
| to do any business validation on a item                 |               |                         | Validator | SpringValidator |

------------------------------------------------------------------------

Sheet 12: *API-ItemReader*
==========================

|     |                                                                                     |            |                              |                         |                                    |                |                                   |          |
|-----|-------------------------------------------------------------------------------------|------------|------------------------------|-------------------------|------------------------------------|----------------|-----------------------------------|----------|
|     |                                                                                     | ItemReader | FlatFileItemReader           |                         |                                    |                |                                   |          |
|     | populte a record data to java domain object                                         |            |                              | LineMapper              | DefaultLineMapper                  |                |                                   |          |
|     | If I want to change tokonizing logic , give custom implementation                   |            |                              |                         |                                    | LineTokenizer  | DelimitedLineTokenizer            |          |
|     | to parse fixed length flat fle                                                      |            |                              |                         |                                    |                | FixedLengthTokenizer              |          |
|     | when a record span more than one line                                               |            |                              |                         |                                    |                | PatternMatchingCompositeTokenizer |          |
|     | it is collection of fiields produced by tokenizer                                   |            |                              |                         |                                    |                |                                   | FieldSet |
|     | it copy value from fieldSet to Domain object                                        |            |                              |                         |                                    | FieldSetMapper | BeanWrapperFieldSetMapper         |          |
|     |                                                                                     |            |                              |                         |                                    |                | PassThroughFieldSetMapper         |          |
|     | read data from JSON data structor                                                   |            |                              |                         | JsonLineMapper                     |                |                                   |          |
|     | a file has more than one formatted line and each to different domain object         |            |                              |                         | PatternMatchingCompositeLineMapper |                |                                   |          |
|     | it just seperate the records either line ending or other means. But not FIELD       |            |                              | RecordSeperatorPolicy   | DefaultRecordSeparatorPolicy       |                |                                   |          |
|     | the file to be read                                                                 |            |                              | Resource                | FileSystemResource                 |                |                                   |          |
|     | calll back when a line being skipped as raw line                                    |            |                              | LineCallbackHandler     |                                    |                |                                   |          |
|     |                                                                                     |            |                              |                         |                                    |                |                                   |          |
|     | for XML as input file                                                               |            | StaxEventItemReader          |                         |                                    |                |                                   |          |
|     | it is from Xstream, used for marshall /unmarshal                                    |            |                              | XstreamMarshaller       |                                    |                |                                   |          |
|     |                                                                                     |            |                              |                         |                                    |                |                                   |          |
|     | to read more than one file as input. File either xml/flat file                      |            | MultiResourceItemReader      |                         |                                    |                |                                   |          |
|     |                                                                                     |            |                              |                         |                                    |                |                                   |          |
|     |                                                                                     |            | JdbcCursorItemReader         |                         |                                    |                |                                   |          |
|     | it is from spring-jdbc                                                              |            |                              | RowMapper               |                                    |                |                                   |          |
|     | get cursor by calling a procedure                                                   |            | StoredProcedureItemReader    |                         |                                    |                |                                   |          |
|     |                                                                                     |            |                              | RowMapper               |                                    |                |                                   |          |
|     | paging instead of cursor                                                            |            | JdbcPagingItemReader         | PagingQueryProvider     | SqlPagingQueryProviderFactoryBean  |                |                                   |          |
|     |                                                                                     |            |                              |                         |                                    |                |                                   |          |
|     | use stateless session                                                               |            | HibernateCursorItemReader    |                         |                                    |                |                                   |          |
|     | it is from hibernate api                                                            |            |                              | HibernateSessionFactory |                                    |                |                                   |          |
|     |                                                                                     |            | HibernatePagingItemReader    |                         |                                    |                |                                   |          |
|     |                                                                                     |            | JpaPagingItemReader          |                         |                                    |                |                                   |          |
|     | from JPA                                                                            |            |                              | EnitityManager          |                                    |                |                                   |          |
|     | it is deprecated in Spring Batch 3.0                                                |            | IbatisPagingItemReader       |                         |                                    |                |                                   |          |
|     | to delegete to existing class for reading.                                          |            | ItemReaderAdapter            |                         |                                    |                |                                   |          |
|     |                                                                                     |            | JmsItemReader                |                         |                                    |                |                                   |          |
|     |                                                                                     |            |                              |                         |                                    |                |                                   |          |
|     | It is common to all also used access execution context by reader, writer, processor | ItemStream |                              |                         |                                    |                |                                   |          |
|     |                                                                                     |            |                              |                         |                                    |                |                                   |          |
|     |                                                                                     |            |                              |                         |                                    |                |                                   |          |
|     | thrown when reading                                                                 |            | FlatFileParseException       |                         |                                    |                |                                   |          |
|     | thrown when tokenize                                                                |            | FlatFileFormatExecption      |                         |                                    |                |                                   |          |
|     | thrown when setting fieldset                                                        |            | InCorrectTokenCountException |                         |                                    |                |                                   |          |
|     | thrown by fixed legth tokenizer                                                     |            | IncorectLineLengthException  |                         |                                    |                |                                   |          |

------------------------------------------------------------------------

Sheet 13: *API-ItemWriter*
==========================

|                                                          |            |                               |                                |                                            |                |                           |
|----------------------------------------------------------|------------|-------------------------------|--------------------------------|--------------------------------------------|----------------|---------------------------|
|                                                          | ItemWriter | FlatFileItemWriter            |                                |                                            |                |                           |
|                                                          |            |                               | Resource                       |                                            |                |                           |
| convert a domain object into a line of output file       |            |                               | LineAggregator                 |                                            |                |                           |
| it simply call toString() on a item                      |            |                               |                                | PassThroughLineAggregator                  |                |                           |
| we have to use this when we have domain object as record |            |                               |                                | ExtractorLineAggregator                    |                |                           |
| write a file with fixed length                           |            |                               |                                | FormatterLineAggregator                    |                |                           |
| write a file with delimited                              |            |                               |                                | DelimitedLineAggregator                    |                |                           |
| it used to write out collection type of array object     |            |                               |                                |                                            | FieldExtractor | BeanWrapperFieldExtractor |
|                                                          |            |                               |                                |                                            |                | PassThroughFieldExtractor |
| write header                                             |            |                               | FlatFileHeaderCallback         |                                            |                |                           |
| write footter                                            |            |                               | FlatFileFooterCallback         |                                            |                |                           |
|                                                          |            |                               |                                |                                            |                |                           |
| to write out put XML file                                |            | StaxEventItemWriter           | StaxWriterCallback             |                                            |                |                           |
|                                                          |            |                               | Marshaller                     | XstreamMarshaller                          |                |                           |
|                                                          |            |                               |                                |                                            |                |                           |
| fill the parameter by ? And index of ?                   |            | JdbcBatchItemWriter           | ItemPreparedStatementSetter    |                                            |                |                           |
| fill the parameter by name                               |            |                               | ItemSqlParameterSourceProvider | BeanPropertyItemSqlParameterSourceProvider |                |                           |
| the datasource configuration                             |            |                               | DataSource                     |                                            |                |                           |
|                                                          |            |                               |                                |                                            |                |                           |
| write data into DB via Hibernate                         |            | HibernateItemWriter           |                                |                                            |                |                           |
| write data into DB via JPA                               |            | JpaItemWriter                 |                                |                                            |                |                           |
| write data into DB via iBATIS                            |            | IbatisBatchItemWriter         |                                |                                            |                |                           |
|                                                          |            |                               |                                |                                            |                |                           |
| to use any existing service to write data out            |            | ItemWriterAdapter             |                                |                                            |                |                           |
| JMS item writer                                          |            | JmsItemWriter                 |                                |                                            |                |                           |
|                                                          |            | SimpleMailMessageItemWriter   |                                |                                            |                |                           |
|                                                          |            |                               |                                |                                            |                |                           |
| it composit and combination of many writers              |            | CompositeItemWriter           |                                |                                            |                |                           |
| to write many output files                               |            | MultiResourceItemWriter       |                                |                                            |                |                           |
|                                                          | Classifier |                               |                                |                                            |                |                           |
|                                                          |            | ClassifierCompositeItemWriter |                                |                                            |                |                           |
|                                                          |            | BackToBackPatternClassifier   |                                |                                            |                |                           |

------------------------------------------------------------------------

Sheet 14: *Spring batch LLR*
============================

|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
|                                                                                                                                                                     | LLR flow                                                                                                       |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     | RC flow                                                                                                        |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     | MAF flow                                                                                                       | **put all the negative condition in where clause , also group by gfrn and fdlacc in SQL itself**                                               |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     | RE-Run flow                                                                                                    |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                | have one step to write failure records                                                                                                         |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                | llr will have non-linear flow,                                                                                                                 |                                     |
|                                                                                                                                                                     |                                                                                                                | use of Exection Context and Data Holder for data sharing between STEPs                                                                         |                                     |
|                                                                                                                                                                     |                                                                                                                | use step-exection listener before and after for reference data load, next step to be run                                                       |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                | **shall i use a hashmap, key as table name, value as records of that tables for reference dtata. It will give more readable in service layer** |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                | meta tables in every Oralce in instance or H2 database                                                                                         |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                | i prefere JobExectionDecider, since i dont want to persist metadata.                                                                           |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                | let s use JobParaaameter from system env variable                                                                                              |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                | let use data holder for sharing data between steps                                                                                             |                                     |
|                                                                                                                                                                     | local parallism                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                | Local Scalling ( Multithreaded Step, Parellel Step )                                                                                           |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                | we use split to run maf and standard deviation job                                                                                             |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                | we use partitioning for LLR and RC Filter                                                                                                      |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     | Master hashmap                                                                                                 |                                                                                                                                                | llr, rc, fclos dto list             |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                | alll control tables                 |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                | any ref.data used more than one job |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     | slave hashmap                                                                                                  |                                                                                                                                                | ever job                            |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                | loaded by steplistener              |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                | cleared by step listener            |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     | make ready H2 database to test completly in local box itself., if need copy neecessary data from oracle to h2  |                                                                                                                                                |                                     |
|                                                                                                                                                                     | H2 it must have duplicate schema of oracle                                                                     |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                | use of ParameterValidator                                                                                                                      |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
| **use of job level listener to load either fclos or lll\_loan exposure**                                                                                            |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     | we will have facility to re-order stepss, skipping steps                                                       |                                                                                                                                                |                                     |
|                                                                                                                                                                     | **Lllr cannot use in-memory job-reposisotry, since it is not support parellel, mulitithreaded step exectioon** |                                                                                                                                                |                                     |
| **So, lets consider H2 database for reposiitory and get benefit of parallel, multithread step**                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     | Write custom jobparamter to validate                                                                           |                                                                                                                                                |                                     |
|                                                                                                                                                                     | WRITE custom jobparameter builder to build from system variable                                                |                                                                                                                                                |                                     |
| manish                                                                                                                                                              | on what column basis, records are indepdent like data category or gfcid, or gfrn lik that                      |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
| **pre proocess put in step listener**                                                                                                                               |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
| adjustement                                                                                                                                                         |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     | call adjustement step only if it has adjustment otherwise skip                                                 |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
| **use jobOperator to stop the batch execution if any exception throrwn by any of service layer**                                                                    |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
| **implement custom of JobParametersIncrementer to increment llr and rc run reference no,, populate llr,rc rundata table also, ALWAYS pass -next parameter**         |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     | lets keep all the llr\_run\_control table values are llr, rc, feed, asofdate as jobparameters                  |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
| Let not use any ExecutionContext, since it persist data...... if it is in-momory—map based....i can use                                                             |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     | lets jave jobparameters to hold object or property of 4 control tables                                         |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
| **as of now all intermediate table commit happening then and there. It must be modified to commit only after complete job both llr and rc table pushed propertly.** |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
| add Transaction manager only those step persist data but not for all the step                                                                                       |                                                                                                                |                                                                                                                                                |                                     |
| SQLite can be used as Jobrepository                                                                                                                                 |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
| service layer no need to be spring bean, if we use MethodInvokingTaskletAdapter                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
| **let use FlatFileItemReader and call read method to read input file. Along with BeanWrapperFieldSetMapper**                                                        |                                                                                                                |                                                                                                                                                |                                     |
|                                                                                                                                                                     |                                                                                                                |                                                                                                                                                |                                     |
| **use of FlatfileItemWriter for standarad deviation csv ( 6) file generation**                                                                                      |                                                                                                                |                                                                                                                                                |                                     |

------------------------------------------------------------------------

Sheet 15: *SpringBatch-SESSION*
===============================

Job

step

Data holder

Context

chunk

Reader

parttition

Writer

parellel execution of a step

Processor/tasklet

parellel execution of many step

remote chunking

SPI

Joblauncher

Testing

JobParameter

JobRepository

Job Status

single run of job

JobExecution

ExecutionContext

Step Status

single run of a step
