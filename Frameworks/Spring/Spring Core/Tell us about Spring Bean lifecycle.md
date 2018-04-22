## Tell us about Spring Bean Lifecycle
1. Instantiate bean through constructor.
2. Populate properties(injection)
3. setBeanName()
	If **BeanNameAware** interface is implemented with setBeanName() method.
4. setBeanFactory()
	If BeanFactoryAware interface is implemented with setBeanFactory() method.
5. setApplicationContext()
	If ApplicationContextAware interace is implemented with setApplicationContext() method.
6. Pre initialization(BeanPostProcessor)
7. custom init() method
8. Post initialization(BeanPostProcessor)
