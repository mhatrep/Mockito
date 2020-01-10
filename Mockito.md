Intent of our testing is to validate the behavior of a class
Mocking techniques should be applied to the external dependencies of the class and not to the class itself.

STUBBING METHOD’S RETURNED VALUE
One of the basic functions of mocking frameworks is an ability to return a given value when a specific method is called. It can be done using Mockito.when() in conjunction with thenReturn () . This process of defining how a given mock method should behave is called stubbing.

Mockito makes heavy use of static methods. It is good to use static imports to make code shorter and more readable. IDE can be used to
automatize adding static imports


# Test Doubles
1. Dummy
2. Fake
3. Stub
4. Mock
Spy - a mock created as a proxy to an existing real object; some
methods can be stubbed, while the un- stubbed ones are forwarded to the covered object
----------------------------------------------------
# Mockito 

Basics. Annotations, 



Mocking in Mockito is performed using when(obj).then*() in the Arrange step.
Later, interaction with our mock can be validated using verify() in the Assert step.

## Enable Mockito - 3 Ways
1. @RunWith(MockitoJUnitRunner.class)
2. MockitoAnnotations.initMocks()
3. MockitoJUnit.rule()

## Mock Methods

1. Simple Mocking
MyList listMock = mock(MyList.class);
when(listMock.add(anyString())).thenReturn(false);
2. Mocking with Mock's Name
3. Mocking with Answer (implements Answer<Boolean> )
4. Mocking with MockSettings

----------------------------------------------------

## ArgumentMatchers - making sure certain arguments were passed to mocks.

ArgumentCaptor may be a better fit if we need it to assert on argument values to complete
verification or our custom argument matcher is not likely to be reused.

Custom argument matchers via ArgumentMatcher are usually better for stubbing.

----------------------------------------------------

@Mock - create and inject mocked instances without having to call Mockito.mock manually
@Spy - spy on an existing instance.
@Captor - create an ArgumentCaptor instance
@InjectMocks - inject mock fields into the tested object automatically.

----------------------------------------------------

Mockito.when(wordMap.get("aWord")).thenReturn("aMeaning");

----------------------------------------------------

Mockito's annotations minimize repetitive mock creation code
They make tests more readable
@InjectMocks is necessary for injecting both @Spy and @Mock instances


## BDDMockito
import static org.mockito.BDDMockito.*;

write our Arrange step using given (instead of when), likewise, we could write our Assert step using then (instead of verify).

----------------------------------------------------

# PowerMock

Mockito cannot:
•	 mock final classes
•	 mock enums
•	 mock final methods
•	 mock static methods
•	 mock private methods
•	 mock hashCode() and equals()

Provides capabilities to work with the Java Reflection API in a simple way to overcome the problems of Mockito, such as the lack of ability to mock final, static or private methods.

@RunWith(PowerMockRunner.class)
Partial Mocking - Partial Class



