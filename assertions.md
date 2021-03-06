### assertion 斷言


### assertTrue

```php
use PHPUnit\Framework\TestCase;

class AssertionsTest extends TestCase 
{
    public function test_assert_true() 
    {
        $actual = false;

        $this->assertTrue($actual);
    }
}
```

### assertFalse

```php
use PHPUnit\Framework\TestCase;

class AssertionsTest extends TestCase 
{
    public function test_assert_false() 
    {
        $actual = false;

        $this->assertFalse($actual);
    }
}
```

### assertEquals

```php
use PHPUnit\Framework\TestCase;

class AssertionsTest extends TestCase 
{
    public function test_assert_equals() 
    {
        $expected = true;
        $actual = true;
        
        $this->assertEquals($expected, $actual);
    }
}
```

### assertSame

```php
use PHPUnit\Framework\TestCase;

class AssertionsTest extends TestCase 
{
    public function test_assert_same() 
    {
        $expected = true;
        $actual = true;
        
        $this->assertSame($expected, $actual);
    }
}
```

### assertContains


#### assertContains (array)

```php
use PHPUnit\Framework\TestCase;

class AssertionsTest extends TestCase 
{
    public function test_assert_contains_array() 
    {
        $needle = 3;
        
        $this->assertContains($needle, [1, 3, 5, 7, 9]);
    }
}
```

#### assertContains (string)

```php
use PHPUnit\Framework\TestCase;

class AssertionsTest extends TestCase 
{
    public function test_assert_contains_string()
    {
        $needle = 'oba';
        
        $this->assertContains($needle, 'foobar');
    }
}
```

### assertCount

```php
use PHPUnit\Framework\TestCase;

class AssertionsTest extends TestCase 
{
    public function test_assert_count() 
    {
        $this->assertCount(5, [1, 3, 5, 7, 9]);
    }
}
```

### assertArrayHasKey

```php
use PHPUnit\Framework\TestCase;

class AssertionsTest extends TestCase 
{
    public function test_assert_array_has_key() 
    {
        $this->assertArrayHasKey('bar', ['bar' => 'baz']);
    }
}
```
    
### assertArraySubset

```php
use PHPUnit\Framework\TestCase;

class AssertionsTest extends TestCase 
{
    public function test_assert_array_subset()
    {
        $this->assertArraySubset(['config' => ['key-a']], ['config' => ['key-a', 'key-c']]);
    }
}
```

### assertInternalType

```php
use PHPUnit\Framework\TestCase;

class AssertionsTest extends TestCase 
{
    public function test_assert_internal_type()
    {
        $this->assertInternalType('numeric', 1);
        $this->assertInternalType('numeric', 1.0);
        $this->assertInternalType('int', 1);
        $this->assertInternalType('float', 1.0);
        $this->assertInternalType('string', '1');
    }
}
```

### assertInstanceOf

```php
use PHPUnit\Framework\TestCase;

class AssertionsTest extends TestCase 
{
    public function test_assert_instance_of()
    {
        $this->assertInstanceOf(stdClass::class, new stdClass);
    }
}
```

### assertJsonStringEqualsJsonString

```php
use PHPUnit\Framework\TestCase;

class AssertionsTest extends TestCase 
{
    public function test_assert_json_string_equals_json_string()
    {
        $this->assertJsonStringEqualsJsonString(
            json_encode(['Mascot' => 'Tux']),
            json_encode(['Mascot' => 'Tux'])
        );
    }
}
```